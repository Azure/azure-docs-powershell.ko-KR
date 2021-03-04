---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 837e0fa40bc07ce5c38d6dfd4b7c86efe2425be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956331"
---
# <span data-ttu-id="ce4db-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="ce4db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce4db-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4db-103">웹후크 ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="ce4db-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce4db-104">SYNTAX</span></span>

### <span data-ttu-id="ce4db-105">ResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce4db-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce4db-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce4db-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4db-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce4db-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce4db-108">설명</span><span class="sxs-lookup"><span data-stu-id="ce4db-108">DESCRIPTION</span></span>
<span data-ttu-id="ce4db-109">Test-AzContainerRegistryWebhook cmdlet은 웹후크 ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="ce4db-110">예제</span><span class="sxs-lookup"><span data-stu-id="ce4db-110">EXAMPLES</span></span>

### <span data-ttu-id="ce4db-111">예제 1: 웹후크 ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="ce4db-112">웹후크 ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="ce4db-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce4db-113">PARAMETERS</span></span>

### <span data-ttu-id="ce4db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4db-114">-DefaultProfile</span></span>
<span data-ttu-id="ce4db-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4db-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ce4db-116">-Name</span></span>
<span data-ttu-id="ce4db-117">웹후크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4db-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ce4db-118">-RegistryName</span></span>
<span data-ttu-id="ce4db-119">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-119">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce4db-120">-ResourceGroupName</span></span>
<span data-ttu-id="ce4db-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4db-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce4db-122">-ResourceId</span></span>
<span data-ttu-id="ce4db-123">컨테이너 레지스트리 Webhook 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ce4db-123">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4db-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-124">-Webhook</span></span>
<span data-ttu-id="ce4db-125">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-125">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4db-126">CommonParameters</span></span>
<span data-ttu-id="ce4db-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4db-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce4db-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4db-129">입력</span><span class="sxs-lookup"><span data-stu-id="ce4db-129">INPUTS</span></span>

### <span data-ttu-id="ce4db-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="ce4db-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ce4db-131">System.String</span></span>

## <span data-ttu-id="ce4db-132">출력</span><span class="sxs-lookup"><span data-stu-id="ce4db-132">OUTPUTS</span></span>

### <span data-ttu-id="ce4db-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="ce4db-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="ce4db-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce4db-134">NOTES</span></span>

## <span data-ttu-id="ce4db-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce4db-135">RELATED LINKS</span></span>

[<span data-ttu-id="ce4db-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ce4db-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ce4db-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ce4db-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce4db-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)