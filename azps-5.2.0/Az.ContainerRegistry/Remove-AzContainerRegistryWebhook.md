---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326801"
---
# <span data-ttu-id="beaf2-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="beaf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="beaf2-103">컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="beaf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="beaf2-104">SYNTAX</span></span>

### <span data-ttu-id="beaf2-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="beaf2-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beaf2-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beaf2-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beaf2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="beaf2-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beaf2-108">설명</span><span class="sxs-lookup"><span data-stu-id="beaf2-108">DESCRIPTION</span></span>
<span data-ttu-id="beaf2-109">Remove-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="beaf2-110">예제</span><span class="sxs-lookup"><span data-stu-id="beaf2-110">EXAMPLES</span></span>

### <span data-ttu-id="beaf2-111">예제 1: 컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="beaf2-112">컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="beaf2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beaf2-113">PARAMETERS</span></span>

### <span data-ttu-id="beaf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaf2-114">-DefaultProfile</span></span>
<span data-ttu-id="beaf2-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beaf2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="beaf2-116">-Name</span></span>
<span data-ttu-id="beaf2-117">웹후크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-117">Webhook Name.</span></span>

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

### <span data-ttu-id="beaf2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="beaf2-118">-PassThru</span></span>
<span data-ttu-id="beaf2-119">제거에 성공하면 이 cmdlet이 true를 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="beaf2-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="beaf2-120">-RegistryName</span></span>
<span data-ttu-id="beaf2-121">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="beaf2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beaf2-122">-ResourceGroupName</span></span>
<span data-ttu-id="beaf2-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="beaf2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="beaf2-124">-ResourceId</span></span>
<span data-ttu-id="beaf2-125">컨테이너 레지스트리 웹후크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="beaf2-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="beaf2-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-126">-Webhook</span></span>
<span data-ttu-id="beaf2-127">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="beaf2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="beaf2-128">-Confirm</span></span>
<span data-ttu-id="beaf2-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beaf2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beaf2-130">-WhatIf</span></span>
<span data-ttu-id="beaf2-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="beaf2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beaf2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beaf2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaf2-133">CommonParameters</span></span>
<span data-ttu-id="beaf2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="beaf2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaf2-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="beaf2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaf2-136">입력</span><span class="sxs-lookup"><span data-stu-id="beaf2-136">INPUTS</span></span>

### <span data-ttu-id="beaf2-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="beaf2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="beaf2-138">System.String</span></span>

## <span data-ttu-id="beaf2-139">출력</span><span class="sxs-lookup"><span data-stu-id="beaf2-139">OUTPUTS</span></span>

### <span data-ttu-id="beaf2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="beaf2-140">System.Boolean</span></span>

## <span data-ttu-id="beaf2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="beaf2-141">NOTES</span></span>

## <span data-ttu-id="beaf2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="beaf2-142">RELATED LINKS</span></span>

[<span data-ttu-id="beaf2-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="beaf2-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="beaf2-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="beaf2-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="beaf2-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)