---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531067"
---
# <span data-ttu-id="a72e8-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="a72e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a72e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a72e8-103">Webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a72e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a72e8-104">SYNTAX</span></span>

### <span data-ttu-id="a72e8-105">ResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a72e8-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a72e8-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a72e8-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a72e8-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a72e8-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a72e8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a72e8-108">DESCRIPTION</span></span>
<span data-ttu-id="a72e8-109">Test-AzureRmContainerRegistryWebhook cmdlet은 webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="a72e8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a72e8-110">EXAMPLES</span></span>

### <span data-ttu-id="a72e8-111">예제 1: webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="a72e8-112">Webhook ping 이벤트를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="a72e8-113">변수</span><span class="sxs-lookup"><span data-stu-id="a72e8-113">PARAMETERS</span></span>

### <span data-ttu-id="a72e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72e8-114">-DefaultProfile</span></span>
<span data-ttu-id="a72e8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72e8-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a72e8-116">-Name</span></span>
<span data-ttu-id="a72e8-117">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="a72e8-117">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72e8-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a72e8-118">-RegistryName</span></span>
<span data-ttu-id="a72e8-119">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="a72e8-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72e8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72e8-122">-ResourceId</span></span>
<span data-ttu-id="a72e8-123">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a72e8-123">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72e8-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-124">-Webhook</span></span>
<span data-ttu-id="a72e8-125">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a72e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72e8-126">CommonParameters</span></span>
<span data-ttu-id="a72e8-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72e8-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a72e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72e8-129">입력</span><span class="sxs-lookup"><span data-stu-id="a72e8-129">INPUTS</span></span>

### <span data-ttu-id="a72e8-130">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="a72e8-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a72e8-131">System.String</span></span>

## <span data-ttu-id="a72e8-132">출력</span><span class="sxs-lookup"><span data-stu-id="a72e8-132">OUTPUTS</span></span>

### <span data-ttu-id="a72e8-133">ContainerRegistry를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a72e8-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="a72e8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a72e8-134">NOTES</span></span>

## <span data-ttu-id="a72e8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a72e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="a72e8-136">새로운 AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a72e8-137">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a72e8-138">업데이트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a72e8-139">제거-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a72e8-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
