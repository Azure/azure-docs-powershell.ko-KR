---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: d2fee7d402ddf25a2bcc4b32528e31e44f500618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535247"
---
# <span data-ttu-id="68953-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="68953-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="68953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68953-102">SYNOPSIS</span></span>
<span data-ttu-id="68953-103">컨테이너 레지스트리 webhook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68953-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68953-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68953-104">SYNTAX</span></span>

### <span data-ttu-id="68953-105">ListWebhookByNameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="68953-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68953-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="68953-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68953-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68953-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68953-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68953-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68953-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68953-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68953-110">설명은</span><span class="sxs-lookup"><span data-stu-id="68953-110">DESCRIPTION</span></span>
<span data-ttu-id="68953-111">Get-AzureRmContainerRegistryWebhook cmdlet은 컨테이너 레지스트리의 지정 된 webhook 또는 컨테이너 레지스트리의 모든 webhooks 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68953-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="68953-112">예제의</span><span class="sxs-lookup"><span data-stu-id="68953-112">EXAMPLES</span></span>

### <span data-ttu-id="68953-113">예제 1: 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="68953-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="68953-114">컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="68953-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="68953-115">예제 2: 컨테이너 레지스트리의 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="68953-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="68953-116">컨테이너 레지스트리의 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="68953-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="68953-117">예제 3: 구성 세부 정보를 사용 하 여 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="68953-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="68953-118">구성 세부 정보를 사용 하 여 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="68953-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="68953-119">변수</span><span class="sxs-lookup"><span data-stu-id="68953-119">PARAMETERS</span></span>

### <span data-ttu-id="68953-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68953-120">-DefaultProfile</span></span>
<span data-ttu-id="68953-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68953-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68953-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="68953-122">-IncludeConfiguration</span></span>
<span data-ttu-id="68953-123">Webhook에 대 한 구성 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68953-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="68953-124">-이름</span><span class="sxs-lookup"><span data-stu-id="68953-124">-Name</span></span>
<span data-ttu-id="68953-125">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="68953-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68953-126">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="68953-126">-Registry</span></span>
<span data-ttu-id="68953-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="68953-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68953-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="68953-128">-RegistryName</span></span>
<span data-ttu-id="68953-129">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68953-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68953-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68953-130">-ResourceGroupName</span></span>
<span data-ttu-id="68953-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68953-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68953-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68953-132">-ResourceId</span></span>
<span data-ttu-id="68953-133">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="68953-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="68953-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68953-134">CommonParameters</span></span>
<span data-ttu-id="68953-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68953-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68953-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68953-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68953-137">입력</span><span class="sxs-lookup"><span data-stu-id="68953-137">INPUTS</span></span>

### <span data-ttu-id="68953-138">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68953-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="68953-139">매개 변수: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68953-139">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="68953-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68953-140">System.String</span></span>

## <span data-ttu-id="68953-141">출력</span><span class="sxs-lookup"><span data-stu-id="68953-141">OUTPUTS</span></span>

### <span data-ttu-id="68953-142">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="68953-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="68953-143">상속자</span><span class="sxs-lookup"><span data-stu-id="68953-143">NOTES</span></span>

## <span data-ttu-id="68953-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68953-144">RELATED LINKS</span></span>

[<span data-ttu-id="68953-145">새로운 AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="68953-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="68953-146">업데이트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="68953-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="68953-147">제거-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="68953-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="68953-148">테스트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="68953-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
