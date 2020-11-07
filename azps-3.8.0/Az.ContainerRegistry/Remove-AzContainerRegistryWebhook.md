---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877909"
---
# <span data-ttu-id="b425b-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b425b-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b425b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b425b-102">SYNOPSIS</span></span>
<span data-ttu-id="b425b-103">컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b425b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b425b-104">SYNTAX</span></span>

### <span data-ttu-id="b425b-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b425b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b425b-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b425b-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b425b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b425b-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b425b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b425b-108">DESCRIPTION</span></span>
<span data-ttu-id="b425b-109">Remove-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="b425b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b425b-110">EXAMPLES</span></span>

### <span data-ttu-id="b425b-111">예제 1: 컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="b425b-112">컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b425b-113">변수</span><span class="sxs-lookup"><span data-stu-id="b425b-113">PARAMETERS</span></span>

### <span data-ttu-id="b425b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b425b-114">-DefaultProfile</span></span>
<span data-ttu-id="b425b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b425b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b425b-116">-Name</span></span>
<span data-ttu-id="b425b-117">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="b425b-117">Webhook Name.</span></span>

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

### <span data-ttu-id="b425b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b425b-118">-PassThru</span></span>
<span data-ttu-id="b425b-119">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b425b-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b425b-120">-RegistryName</span></span>
<span data-ttu-id="b425b-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="b425b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b425b-122">-ResourceGroupName</span></span>
<span data-ttu-id="b425b-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b425b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b425b-124">-ResourceId</span></span>
<span data-ttu-id="b425b-125">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="b425b-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b425b-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="b425b-126">-Webhook</span></span>
<span data-ttu-id="b425b-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="b425b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b425b-128">-Confirm</span></span>
<span data-ttu-id="b425b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b425b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b425b-130">-WhatIf</span></span>
<span data-ttu-id="b425b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b425b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b425b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b425b-133">CommonParameters</span></span>
<span data-ttu-id="b425b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b425b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b425b-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b425b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b425b-136">입력</span><span class="sxs-lookup"><span data-stu-id="b425b-136">INPUTS</span></span>

### <span data-ttu-id="b425b-137">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b425b-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="b425b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b425b-138">System.String</span></span>

## <span data-ttu-id="b425b-139">출력</span><span class="sxs-lookup"><span data-stu-id="b425b-139">OUTPUTS</span></span>

### <span data-ttu-id="b425b-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b425b-140">System.Boolean</span></span>

## <span data-ttu-id="b425b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b425b-141">NOTES</span></span>

## <span data-ttu-id="b425b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b425b-142">RELATED LINKS</span></span>

[<span data-ttu-id="b425b-143">새로운 AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b425b-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b425b-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b425b-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b425b-145">업데이트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b425b-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b425b-146">테스트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b425b-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)