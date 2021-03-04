---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: e189be8f04081bbc51c5cc19b981c164ce4e9c2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956395"
---
# <span data-ttu-id="55466-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="55466-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="55466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55466-102">SYNOPSIS</span></span>
<span data-ttu-id="55466-103">컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="55466-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="55466-104">구문</span><span class="sxs-lookup"><span data-stu-id="55466-104">SYNTAX</span></span>

### <span data-ttu-id="55466-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="55466-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55466-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55466-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55466-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55466-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55466-108">설명</span><span class="sxs-lookup"><span data-stu-id="55466-108">DESCRIPTION</span></span>
<span data-ttu-id="55466-109">Remove-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="55466-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="55466-110">예제</span><span class="sxs-lookup"><span data-stu-id="55466-110">EXAMPLES</span></span>

### <span data-ttu-id="55466-111">예제 1: 컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="55466-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="55466-112">컨테이너 레지스트리 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="55466-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="55466-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="55466-113">PARAMETERS</span></span>

### <span data-ttu-id="55466-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55466-114">-DefaultProfile</span></span>
<span data-ttu-id="55466-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55466-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55466-116">-Name</span><span class="sxs-lookup"><span data-stu-id="55466-116">-Name</span></span>
<span data-ttu-id="55466-117">웹후크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55466-117">Webhook Name.</span></span>

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

### <span data-ttu-id="55466-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55466-118">-PassThru</span></span>
<span data-ttu-id="55466-119">제거가 성공한 경우 이 cmdlet이 true를 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55466-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="55466-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="55466-120">-RegistryName</span></span>
<span data-ttu-id="55466-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55466-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="55466-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55466-122">-ResourceGroupName</span></span>
<span data-ttu-id="55466-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55466-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="55466-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55466-124">-ResourceId</span></span>
<span data-ttu-id="55466-125">컨테이너 레지스트리 Webhook 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="55466-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="55466-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="55466-126">-Webhook</span></span>
<span data-ttu-id="55466-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="55466-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="55466-128">-확인</span><span class="sxs-lookup"><span data-stu-id="55466-128">-Confirm</span></span>
<span data-ttu-id="55466-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55466-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55466-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55466-130">-WhatIf</span></span>
<span data-ttu-id="55466-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="55466-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55466-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55466-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55466-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55466-133">CommonParameters</span></span>
<span data-ttu-id="55466-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55466-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55466-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55466-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55466-136">입력</span><span class="sxs-lookup"><span data-stu-id="55466-136">INPUTS</span></span>

### <span data-ttu-id="55466-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="55466-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="55466-138">System.String</span><span class="sxs-lookup"><span data-stu-id="55466-138">System.String</span></span>

## <span data-ttu-id="55466-139">출력</span><span class="sxs-lookup"><span data-stu-id="55466-139">OUTPUTS</span></span>

### <span data-ttu-id="55466-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55466-140">System.Boolean</span></span>

## <span data-ttu-id="55466-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55466-141">NOTES</span></span>

## <span data-ttu-id="55466-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55466-142">RELATED LINKS</span></span>

[<span data-ttu-id="55466-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="55466-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="55466-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="55466-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="55466-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="55466-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="55466-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="55466-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)