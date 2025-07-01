<script>
	import FeatureCard from "$lib/components/FeatureCard.svelte";


  const features = [
    {
      color: "bg-pink-600",
      icon: "📁",
      title: "Collection Base",
      subtitle: "All your content, organized",
    },
    {
      color: "bg-sky-600",
      icon: "📝",
      title: "Form Snap",
      subtitle: "Capture and manage forms",
    },
    {
      color: "bg-blue-500",
      icon: "🌐",
      title: "Site Kit",
      subtitle: "Build and manage your website",
    },
    {
      color: "bg-purple-600",
      icon: "📂",
      title: "Domain Manager",
      subtitle: "Manage your domains effortlessly",
    },
    {
      color: "bg-green-600",
      icon: "📦",
      title: "Store Box",
      subtitle: "Safe and easy storage",
    },
    {
      color: "bg-indigo-600",
      icon: "💡",
      title: "Memory Vault",
      subtitle: "Never forget a thing",
    },
    {
      color: "bg-orange-600",
      icon: "💬",
      title: "Chat Dock",
      subtitle: "Talk with your visitors, instantly",
    },
  ];
</script>

<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 p-4 bg-gray-900 min-h-screen">
  {#each features as feature}
    <FeatureCard
      color={feature.color}
      icon={feature.icon}
      title={feature.title}
      subtitle={feature.subtitle}
    />
  {/each}
</div>
