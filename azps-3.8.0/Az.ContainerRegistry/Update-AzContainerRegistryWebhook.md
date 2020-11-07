---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877885"
---
# <span data-ttu-id="a7e49-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="a7e49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e49-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e49-103">컨테이너 레지스트리 webhook을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="a7e49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7e49-104">SYNTAX</span></span>

### <span data-ttu-id="a7e49-105">ResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7e49-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7e49-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7e49-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7e49-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7e49-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e49-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a7e49-108">DESCRIPTION</span></span>
<span data-ttu-id="a7e49-109">Update-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 webhook을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="a7e49-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a7e49-110">EXAMPLES</span></span>

### <span data-ttu-id="a7e49-111">예제 1: 기존 컨테이너 레지스트리 webhook을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="a7e49-112">기존 컨테이너 레지스트리 webhook을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="a7e49-113">변수</span><span class="sxs-lookup"><span data-stu-id="a7e49-113">PARAMETERS</span></span>

### <span data-ttu-id="a7e49-114">-작업</span><span class="sxs-lookup"><span data-stu-id="a7e49-114">-Action</span></span>
<span data-ttu-id="a7e49-115">Webhook을 포스트백으로 알리기 위한 작업의 공백으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="a7e49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e49-116">-DefaultProfile</span></span>
<span data-ttu-id="a7e49-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e49-118">-헤더</span><span class="sxs-lookup"><span data-stu-id="a7e49-118">-Header</span></span>
<span data-ttu-id="a7e49-119">' Key \[ = value \] ' 형식으로 webhook 알림에 추가 되는 공백으로 구분 된 사용자 지정 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="a7e49-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a7e49-120">-Name</span></span>
<span data-ttu-id="a7e49-121">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="a7e49-121">Webhook Name.</span></span>

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

### <span data-ttu-id="a7e49-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a7e49-122">-RegistryName</span></span>
<span data-ttu-id="a7e49-123">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="a7e49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e49-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7e49-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a7e49-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7e49-126">-ResourceId</span></span>
<span data-ttu-id="a7e49-127">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a7e49-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a7e49-128">-범위</span><span class="sxs-lookup"><span data-stu-id="a7e49-128">-Scope</span></span>
<span data-ttu-id="a7e49-129">Webhook 범위.</span><span class="sxs-lookup"><span data-stu-id="a7e49-129">Webhook scope.</span></span>

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

### <span data-ttu-id="a7e49-130">-상태</span><span class="sxs-lookup"><span data-stu-id="a7e49-130">-Status</span></span>
<span data-ttu-id="a7e49-131">Webhook 상태</span><span class="sxs-lookup"><span data-stu-id="a7e49-131">Webhook status</span></span>

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

### <span data-ttu-id="a7e49-132">태그</span><span class="sxs-lookup"><span data-stu-id="a7e49-132">-Tag</span></span>
<span data-ttu-id="a7e49-133">' Key = value ' 형식으로 구분 된 태그 공간 \[ \] 입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="a7e49-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="a7e49-134">-Uri</span></span>
<span data-ttu-id="a7e49-135">알림을 게시할 webhook에 대 한 서비스 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="a7e49-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-136">-Webhook</span></span>
<span data-ttu-id="a7e49-137">컨테이너 레지스트리 Webhook 개체.</span><span class="sxs-lookup"><span data-stu-id="a7e49-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="a7e49-138">-확인</span><span class="sxs-lookup"><span data-stu-id="a7e49-138">-Confirm</span></span>
<span data-ttu-id="a7e49-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e49-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e49-140">-WhatIf</span></span>
<span data-ttu-id="a7e49-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7e49-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e49-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e49-143">CommonParameters</span></span>
<span data-ttu-id="a7e49-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7e49-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e49-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7e49-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e49-146">입력</span><span class="sxs-lookup"><span data-stu-id="a7e49-146">INPUTS</span></span>

### <span data-ttu-id="a7e49-147">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="a7e49-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7e49-148">System.String</span></span>

## <span data-ttu-id="a7e49-149">출력</span><span class="sxs-lookup"><span data-stu-id="a7e49-149">OUTPUTS</span></span>

### <span data-ttu-id="a7e49-150">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="a7e49-151">상속자</span><span class="sxs-lookup"><span data-stu-id="a7e49-151">NOTES</span></span>

## <span data-ttu-id="a7e49-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7e49-152">RELATED LINKS</span></span>

[<span data-ttu-id="a7e49-153">새로운 AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a7e49-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a7e49-155">테스트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a7e49-156">제거-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a7e49-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)