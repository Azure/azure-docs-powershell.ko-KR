---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495841"
---
# <span data-ttu-id="aa88c-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="aa88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa88c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa88c-103">컨테이너 레지스트리 웹후크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="aa88c-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa88c-104">SYNTAX</span></span>

### <span data-ttu-id="aa88c-105">ResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa88c-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa88c-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa88c-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa88c-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa88c-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa88c-108">설명</span><span class="sxs-lookup"><span data-stu-id="aa88c-108">DESCRIPTION</span></span>
<span data-ttu-id="aa88c-109">이 Update-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 웹후크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="aa88c-110">예제</span><span class="sxs-lookup"><span data-stu-id="aa88c-110">EXAMPLES</span></span>

### <span data-ttu-id="aa88c-111">예제 1: 기존 컨테이너 레지스트리 웹후크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="aa88c-112">기존 컨테이너 레지스트리 웹후크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="aa88c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa88c-113">PARAMETERS</span></span>

### <span data-ttu-id="aa88c-114">-Action</span><span class="sxs-lookup"><span data-stu-id="aa88c-114">-Action</span></span>
<span data-ttu-id="aa88c-115">알림을 게시하기 위해 웹후크를 트리거하는 공백으로 구분된 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa88c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa88c-116">-DefaultProfile</span></span>
<span data-ttu-id="aa88c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa88c-118">-Header</span><span class="sxs-lookup"><span data-stu-id="aa88c-118">-Header</span></span>
<span data-ttu-id="aa88c-119">웹후크 알림에 추가될 'key =value' 형식의 공백으로 구분된 사용자 지정 \[ \] 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="aa88c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa88c-120">-Name</span></span>
<span data-ttu-id="aa88c-121">웹후크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-121">Webhook Name.</span></span>

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

### <span data-ttu-id="aa88c-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="aa88c-122">-RegistryName</span></span>
<span data-ttu-id="aa88c-123">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="aa88c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa88c-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa88c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa88c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa88c-126">-ResourceId</span></span>
<span data-ttu-id="aa88c-127">컨테이너 레지스트리 웹후크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="aa88c-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="aa88c-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="aa88c-128">-Scope</span></span>
<span data-ttu-id="aa88c-129">웹후크 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-129">Webhook scope.</span></span>

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

### <span data-ttu-id="aa88c-130">-Status</span><span class="sxs-lookup"><span data-stu-id="aa88c-130">-Status</span></span>
<span data-ttu-id="aa88c-131">웹후크 상태</span><span class="sxs-lookup"><span data-stu-id="aa88c-131">Webhook status</span></span>

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

### <span data-ttu-id="aa88c-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa88c-132">-Tag</span></span>
<span data-ttu-id="aa88c-133">'key =value' 형식의 공백으로 \[ \] 구분된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="aa88c-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="aa88c-134">-Uri</span></span>
<span data-ttu-id="aa88c-135">알림을 게시할 웹후크에 대한 서비스 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa88c-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-136">-Webhook</span></span>
<span data-ttu-id="aa88c-137">Container Registry 웹후크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="aa88c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa88c-138">-Confirm</span></span>
<span data-ttu-id="aa88c-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa88c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa88c-140">-WhatIf</span></span>
<span data-ttu-id="aa88c-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aa88c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa88c-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa88c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa88c-143">CommonParameters</span></span>
<span data-ttu-id="aa88c-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa88c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa88c-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa88c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa88c-146">입력</span><span class="sxs-lookup"><span data-stu-id="aa88c-146">INPUTS</span></span>

### <span data-ttu-id="aa88c-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="aa88c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="aa88c-148">System.String</span></span>

## <span data-ttu-id="aa88c-149">출력</span><span class="sxs-lookup"><span data-stu-id="aa88c-149">OUTPUTS</span></span>

### <span data-ttu-id="aa88c-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="aa88c-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa88c-151">NOTES</span></span>

## <span data-ttu-id="aa88c-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa88c-152">RELATED LINKS</span></span>

[<span data-ttu-id="aa88c-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="aa88c-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="aa88c-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="aa88c-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="aa88c-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)