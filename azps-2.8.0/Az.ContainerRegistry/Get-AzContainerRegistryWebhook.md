---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: b01b2e8152d74fda5faff36221ffa9b6e75ffcbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697131"
---
# <span data-ttu-id="fc797-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc797-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="fc797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc797-102">SYNOPSIS</span></span>
<span data-ttu-id="fc797-103">컨테이너 레지스트리 webhook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="fc797-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc797-104">SYNTAX</span></span>

### <span data-ttu-id="fc797-105">ListWebhookByNameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc797-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc797-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc797-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc797-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc797-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc797-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc797-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc797-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc797-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc797-110">설명은</span><span class="sxs-lookup"><span data-stu-id="fc797-110">DESCRIPTION</span></span>
<span data-ttu-id="fc797-111">Get-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리의 지정 된 webhook 또는 컨테이너 레지스트리의 모든 webhooks 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="fc797-112">예제의</span><span class="sxs-lookup"><span data-stu-id="fc797-112">EXAMPLES</span></span>

### <span data-ttu-id="fc797-113">예제 1: 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc797-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="fc797-114">컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc797-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="fc797-115">예제 2: 컨테이너 레지스트리의 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc797-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="fc797-116">컨테이너 레지스트리의 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc797-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="fc797-117">예제 3: 구성 세부 정보를 사용 하 여 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc797-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="fc797-118">구성 세부 정보를 사용 하 여 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc797-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="fc797-119">변수</span><span class="sxs-lookup"><span data-stu-id="fc797-119">PARAMETERS</span></span>

### <span data-ttu-id="fc797-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc797-120">-DefaultProfile</span></span>
<span data-ttu-id="fc797-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc797-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc797-122">-IncludeConfiguration</span></span>
<span data-ttu-id="fc797-123">Webhook에 대 한 구성 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="fc797-124">-이름</span><span class="sxs-lookup"><span data-stu-id="fc797-124">-Name</span></span>
<span data-ttu-id="fc797-125">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="fc797-125">Webhook Name.</span></span>

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

### <span data-ttu-id="fc797-126">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="fc797-126">-Registry</span></span>
<span data-ttu-id="fc797-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="fc797-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fc797-128">-RegistryName</span></span>
<span data-ttu-id="fc797-129">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="fc797-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc797-130">-ResourceGroupName</span></span>
<span data-ttu-id="fc797-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc797-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc797-132">-ResourceId</span></span>
<span data-ttu-id="fc797-133">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="fc797-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fc797-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc797-134">CommonParameters</span></span>
<span data-ttu-id="fc797-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc797-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc797-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc797-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc797-137">입력</span><span class="sxs-lookup"><span data-stu-id="fc797-137">INPUTS</span></span>

### <span data-ttu-id="fc797-138">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fc797-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="fc797-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc797-139">System.String</span></span>

## <span data-ttu-id="fc797-140">출력</span><span class="sxs-lookup"><span data-stu-id="fc797-140">OUTPUTS</span></span>

### <span data-ttu-id="fc797-141">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc797-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="fc797-142">상속자</span><span class="sxs-lookup"><span data-stu-id="fc797-142">NOTES</span></span>

## <span data-ttu-id="fc797-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc797-143">RELATED LINKS</span></span>

[<span data-ttu-id="fc797-144">새로운 AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc797-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fc797-145">업데이트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc797-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fc797-146">제거-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc797-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fc797-147">테스트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc797-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)