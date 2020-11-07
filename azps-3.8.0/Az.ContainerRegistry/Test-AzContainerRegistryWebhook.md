---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877886"
---
# <span data-ttu-id="4d6cd-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="4d6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6cd-103">Webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="4d6cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d6cd-104">SYNTAX</span></span>

### <span data-ttu-id="4d6cd-105">ResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d6cd-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d6cd-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6cd-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d6cd-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6cd-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d6cd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4d6cd-108">DESCRIPTION</span></span>
<span data-ttu-id="4d6cd-109">Test-AzContainerRegistryWebhook cmdlet은 webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="4d6cd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4d6cd-110">EXAMPLES</span></span>

### <span data-ttu-id="4d6cd-111">예제 1: webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="4d6cd-112">Webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="4d6cd-113">변수</span><span class="sxs-lookup"><span data-stu-id="4d6cd-113">PARAMETERS</span></span>

### <span data-ttu-id="4d6cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6cd-114">-DefaultProfile</span></span>
<span data-ttu-id="4d6cd-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d6cd-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4d6cd-116">-Name</span></span>
<span data-ttu-id="4d6cd-117">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-117">Webhook Name.</span></span>

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

### <span data-ttu-id="4d6cd-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4d6cd-118">-RegistryName</span></span>
<span data-ttu-id="4d6cd-119">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="4d6cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d6cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d6cd-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="4d6cd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d6cd-122">-ResourceId</span></span>
<span data-ttu-id="4d6cd-123">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="4d6cd-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="4d6cd-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-124">-Webhook</span></span>
<span data-ttu-id="4d6cd-125">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="4d6cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6cd-126">CommonParameters</span></span>
<span data-ttu-id="4d6cd-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6cd-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d6cd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6cd-129">입력</span><span class="sxs-lookup"><span data-stu-id="4d6cd-129">INPUTS</span></span>

### <span data-ttu-id="4d6cd-130">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="4d6cd-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4d6cd-131">System.String</span></span>

## <span data-ttu-id="4d6cd-132">출력</span><span class="sxs-lookup"><span data-stu-id="4d6cd-132">OUTPUTS</span></span>

### <span data-ttu-id="4d6cd-133">ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="4d6cd-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="4d6cd-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4d6cd-134">NOTES</span></span>

## <span data-ttu-id="4d6cd-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d6cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="4d6cd-136">새로운 AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4d6cd-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4d6cd-138">업데이트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4d6cd-139">제거-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d6cd-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)