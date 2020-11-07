---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhookevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
ms.openlocfilehash: b30df9c2cce1c4284085b683a06327e4c0ac3ab0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701182"
---
# <span data-ttu-id="7c519-101">Get-AzContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="7c519-101">Get-AzContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="7c519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c519-102">SYNOPSIS</span></span>
<span data-ttu-id="7c519-103">컨테이너 레지스트리 webhook의 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-103">Gets events of a container registry webhook.</span></span>

## <span data-ttu-id="7c519-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c519-104">SYNTAX</span></span>

### <span data-ttu-id="7c519-105">ListWebhookEventsByNameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c519-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c519-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c519-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c519-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c519-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c519-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c519-108">DESCRIPTION</span></span>
<span data-ttu-id="7c519-109">Get-AzContainerRegistryWebhookEvent cmdlet은 webhook의 모든 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-109">The Get-AzContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="7c519-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c519-110">EXAMPLES</span></span>

### <span data-ttu-id="7c519-111">예제 1: webhook의 모든 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="7c519-112">Webhook의 모든 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="7c519-113">변수</span><span class="sxs-lookup"><span data-stu-id="7c519-113">PARAMETERS</span></span>

### <span data-ttu-id="7c519-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c519-114">-DefaultProfile</span></span>
<span data-ttu-id="7c519-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c519-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7c519-116">-RegistryName</span></span>
<span data-ttu-id="7c519-117">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c519-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c519-118">-ResourceGroupName</span></span>
<span data-ttu-id="7c519-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c519-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c519-120">-ResourceId</span></span>
<span data-ttu-id="7c519-121">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="7c519-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="7c519-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="7c519-122">-Webhook</span></span>
<span data-ttu-id="7c519-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c519-124">-WebhookName</span><span class="sxs-lookup"><span data-stu-id="7c519-124">-WebhookName</span></span>
<span data-ttu-id="7c519-125">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="7c519-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c519-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c519-126">CommonParameters</span></span>
<span data-ttu-id="7c519-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c519-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c519-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c519-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c519-129">입력</span><span class="sxs-lookup"><span data-stu-id="7c519-129">INPUTS</span></span>

### <span data-ttu-id="7c519-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c519-130">System.String</span></span>

## <span data-ttu-id="7c519-131">출력</span><span class="sxs-lookup"><span data-stu-id="7c519-131">OUTPUTS</span></span>

### <span data-ttu-id="7c519-132">ContainerRegistry. PSContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="7c519-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="7c519-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7c519-133">NOTES</span></span>

## <span data-ttu-id="7c519-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c519-134">RELATED LINKS</span></span>

[<span data-ttu-id="7c519-135">새로운 AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c519-135">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c519-136">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c519-136">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c519-137">업데이트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c519-137">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c519-138">제거-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c519-138">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c519-139">테스트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c519-139">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

