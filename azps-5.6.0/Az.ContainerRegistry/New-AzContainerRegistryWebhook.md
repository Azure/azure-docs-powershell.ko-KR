---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 10acca5a89c4ea84d475e5eea2e89e18942116f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975456"
---
# <span data-ttu-id="f98ef-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f98ef-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="f98ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f98ef-103">컨테이너 레지스트리 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="f98ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="f98ef-104">SYNTAX</span></span>

### <span data-ttu-id="f98ef-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f98ef-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f98ef-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ef-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98ef-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ef-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98ef-108">설명</span><span class="sxs-lookup"><span data-stu-id="f98ef-108">DESCRIPTION</span></span>
<span data-ttu-id="f98ef-109">New-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="f98ef-110">예제</span><span class="sxs-lookup"><span data-stu-id="f98ef-110">EXAMPLES</span></span>

### <span data-ttu-id="f98ef-111">예제 1: 컨테이너 레지스트리 웹후크 만들기</span><span class="sxs-lookup"><span data-stu-id="f98ef-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="f98ef-112">컨테이너 레지스트리 웹후크를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="f98ef-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f98ef-113">PARAMETERS</span></span>

### <span data-ttu-id="f98ef-114">-Action</span><span class="sxs-lookup"><span data-stu-id="f98ef-114">-Action</span></span>
<span data-ttu-id="f98ef-115">알림을 게시하기 위해 웹후크를 트리거하는 작업의 공간 구분 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98ef-116">-DefaultProfile</span></span>
<span data-ttu-id="f98ef-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f98ef-118">-헤더</span><span class="sxs-lookup"><span data-stu-id="f98ef-118">-Header</span></span>
<span data-ttu-id="f98ef-119">웹후크 알림에 추가될 사용자 지정 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f98ef-120">-Location</span></span>
<span data-ttu-id="f98ef-121">웹후크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-121">Webhook Location.</span></span>
<span data-ttu-id="f98ef-122">레지스트리의 위치를 기본값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f98ef-123">-Name</span></span>
<span data-ttu-id="f98ef-124">웹후크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="f98ef-125">-Registry</span></span>
<span data-ttu-id="f98ef-126">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f98ef-127">-RegistryName</span></span>
<span data-ttu-id="f98ef-128">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="f98ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="f98ef-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="f98ef-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f98ef-131">-ResourceId</span></span>
<span data-ttu-id="f98ef-132">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f98ef-132">The container registry resource id</span></span>

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

### <span data-ttu-id="f98ef-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="f98ef-133">-Scope</span></span>
<span data-ttu-id="f98ef-134">웹후크 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-135">-Status</span><span class="sxs-lookup"><span data-stu-id="f98ef-135">-Status</span></span>
<span data-ttu-id="f98ef-136">Webhook 상태, 기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="f98ef-137">-Tag</span></span>
<span data-ttu-id="f98ef-138">웹후크 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="f98ef-139">-Uri</span></span>
<span data-ttu-id="f98ef-140">알림을 게시할 웹후크에 대한 서비스 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-141">-확인</span><span class="sxs-lookup"><span data-stu-id="f98ef-141">-Confirm</span></span>
<span data-ttu-id="f98ef-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98ef-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98ef-143">-WhatIf</span></span>
<span data-ttu-id="f98ef-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98ef-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98ef-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98ef-146">CommonParameters</span></span>
<span data-ttu-id="f98ef-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98ef-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f98ef-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98ef-149">입력</span><span class="sxs-lookup"><span data-stu-id="f98ef-149">INPUTS</span></span>

### <span data-ttu-id="f98ef-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f98ef-150">System.String</span></span>

## <span data-ttu-id="f98ef-151">출력</span><span class="sxs-lookup"><span data-stu-id="f98ef-151">OUTPUTS</span></span>

### <span data-ttu-id="f98ef-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f98ef-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="f98ef-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f98ef-153">NOTES</span></span>

## <span data-ttu-id="f98ef-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f98ef-154">RELATED LINKS</span></span>

[<span data-ttu-id="f98ef-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f98ef-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f98ef-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f98ef-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f98ef-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f98ef-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f98ef-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f98ef-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)