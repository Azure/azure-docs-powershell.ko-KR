---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531077"
---
# <span data-ttu-id="339b9-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="339b9-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="339b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339b9-102">SYNOPSIS</span></span>
<span data-ttu-id="339b9-103">컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="339b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="339b9-104">SYNTAX</span></span>

### <span data-ttu-id="339b9-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="339b9-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="339b9-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="339b9-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339b9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="339b9-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339b9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="339b9-108">DESCRIPTION</span></span>
<span data-ttu-id="339b9-109">New-AzureRmContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="339b9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="339b9-110">EXAMPLES</span></span>

### <span data-ttu-id="339b9-111">예제 1: 컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="339b9-112">컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="339b9-113">변수</span><span class="sxs-lookup"><span data-stu-id="339b9-113">PARAMETERS</span></span>

### <span data-ttu-id="339b9-114">-작업</span><span class="sxs-lookup"><span data-stu-id="339b9-114">-Action</span></span>
<span data-ttu-id="339b9-115">Webhook을 포스트백으로 알리기 위한 작업의 공백으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-116">-확인</span><span class="sxs-lookup"><span data-stu-id="339b9-116">-Confirm</span></span>
<span data-ttu-id="339b9-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339b9-118">-DefaultProfile</span></span>
<span data-ttu-id="339b9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="339b9-120">-헤더</span><span class="sxs-lookup"><span data-stu-id="339b9-120">-Header</span></span>
<span data-ttu-id="339b9-121">Webhook 알림에 추가 되는 사용자 지정 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-122">-위치</span><span class="sxs-lookup"><span data-stu-id="339b9-122">-Location</span></span>
<span data-ttu-id="339b9-123">Webhook 위치.</span><span class="sxs-lookup"><span data-stu-id="339b9-123">Webhook Location.</span></span>
<span data-ttu-id="339b9-124">기본값은 레지스트리의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-125">-이름</span><span class="sxs-lookup"><span data-stu-id="339b9-125">-Name</span></span>
<span data-ttu-id="339b9-126">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="339b9-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-127">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="339b9-127">-Registry</span></span>
<span data-ttu-id="339b9-128">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-129">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="339b9-129">-RegistryName</span></span>
<span data-ttu-id="339b9-130">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-130">Container Registry Name.</span></span>

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

### <span data-ttu-id="339b9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339b9-131">-ResourceGroupName</span></span>
<span data-ttu-id="339b9-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="339b9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="339b9-133">-ResourceId</span></span>
<span data-ttu-id="339b9-134">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="339b9-134">The container registry resource id</span></span>

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

### <span data-ttu-id="339b9-135">-범위</span><span class="sxs-lookup"><span data-stu-id="339b9-135">-Scope</span></span>
<span data-ttu-id="339b9-136">Webhook 범위.</span><span class="sxs-lookup"><span data-stu-id="339b9-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-137">-상태</span><span class="sxs-lookup"><span data-stu-id="339b9-137">-Status</span></span>
<span data-ttu-id="339b9-138">Webhook 상태, default 값이 사용 하도록 설정 됨</span><span class="sxs-lookup"><span data-stu-id="339b9-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-139">태그</span><span class="sxs-lookup"><span data-stu-id="339b9-139">-Tag</span></span>
<span data-ttu-id="339b9-140">Webhook 태그.</span><span class="sxs-lookup"><span data-stu-id="339b9-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-141">-Uri</span><span class="sxs-lookup"><span data-stu-id="339b9-141">-Uri</span></span>
<span data-ttu-id="339b9-142">알림을 게시할 webhook에 대 한 서비스 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339b9-143">-WhatIf</span></span>
<span data-ttu-id="339b9-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339b9-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339b9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339b9-146">CommonParameters</span></span>
<span data-ttu-id="339b9-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="339b9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339b9-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339b9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339b9-149">입력</span><span class="sxs-lookup"><span data-stu-id="339b9-149">INPUTS</span></span>

### <span data-ttu-id="339b9-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="339b9-150">System.String</span></span>

## <span data-ttu-id="339b9-151">출력</span><span class="sxs-lookup"><span data-stu-id="339b9-151">OUTPUTS</span></span>

### <span data-ttu-id="339b9-152">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="339b9-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="339b9-153">상속자</span><span class="sxs-lookup"><span data-stu-id="339b9-153">NOTES</span></span>

## <span data-ttu-id="339b9-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="339b9-154">RELATED LINKS</span></span>

[<span data-ttu-id="339b9-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="339b9-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="339b9-156">업데이트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="339b9-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="339b9-157">제거-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="339b9-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="339b9-158">테스트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="339b9-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
