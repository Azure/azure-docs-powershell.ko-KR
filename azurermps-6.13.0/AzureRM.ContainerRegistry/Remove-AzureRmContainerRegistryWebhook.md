---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704155"
---
# <span data-ttu-id="77184-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="77184-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="77184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77184-102">SYNOPSIS</span></span>
<span data-ttu-id="77184-103">컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77184-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77184-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77184-104">SYNTAX</span></span>

### <span data-ttu-id="77184-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="77184-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77184-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77184-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77184-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77184-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77184-108">설명은</span><span class="sxs-lookup"><span data-stu-id="77184-108">DESCRIPTION</span></span>
<span data-ttu-id="77184-109">Remove-AzureRmContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77184-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="77184-110">예제의</span><span class="sxs-lookup"><span data-stu-id="77184-110">EXAMPLES</span></span>

### <span data-ttu-id="77184-111">예제 1: 컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77184-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="77184-112">컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77184-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="77184-113">변수</span><span class="sxs-lookup"><span data-stu-id="77184-113">PARAMETERS</span></span>

### <span data-ttu-id="77184-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77184-114">-DefaultProfile</span></span>
<span data-ttu-id="77184-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77184-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77184-116">-이름</span><span class="sxs-lookup"><span data-stu-id="77184-116">-Name</span></span>
<span data-ttu-id="77184-117">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="77184-117">Webhook Name.</span></span>

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

### <span data-ttu-id="77184-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77184-118">-PassThru</span></span>
<span data-ttu-id="77184-119">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="77184-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77184-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="77184-120">-RegistryName</span></span>
<span data-ttu-id="77184-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77184-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="77184-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77184-122">-ResourceGroupName</span></span>
<span data-ttu-id="77184-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77184-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="77184-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77184-124">-ResourceId</span></span>
<span data-ttu-id="77184-125">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="77184-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="77184-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="77184-126">-Webhook</span></span>
<span data-ttu-id="77184-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="77184-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="77184-128">-확인</span><span class="sxs-lookup"><span data-stu-id="77184-128">-Confirm</span></span>
<span data-ttu-id="77184-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77184-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77184-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77184-130">-WhatIf</span></span>
<span data-ttu-id="77184-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77184-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77184-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77184-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77184-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77184-133">CommonParameters</span></span>
<span data-ttu-id="77184-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77184-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77184-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77184-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77184-136">입력</span><span class="sxs-lookup"><span data-stu-id="77184-136">INPUTS</span></span>

### <span data-ttu-id="77184-137">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="77184-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="77184-138">매개 변수: Webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77184-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="77184-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77184-139">System.String</span></span>

## <span data-ttu-id="77184-140">출력</span><span class="sxs-lookup"><span data-stu-id="77184-140">OUTPUTS</span></span>

### <span data-ttu-id="77184-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="77184-141">System.Boolean</span></span>

## <span data-ttu-id="77184-142">상속자</span><span class="sxs-lookup"><span data-stu-id="77184-142">NOTES</span></span>

## <span data-ttu-id="77184-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77184-143">RELATED LINKS</span></span>

[<span data-ttu-id="77184-144">새로운 AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="77184-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="77184-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="77184-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="77184-146">업데이트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="77184-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="77184-147">테스트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="77184-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
