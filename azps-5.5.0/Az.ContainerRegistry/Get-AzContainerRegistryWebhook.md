---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181468"
---
# <span data-ttu-id="d05e9-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d05e9-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="d05e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d05e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d05e9-103">컨테이너 레지스트리 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="d05e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="d05e9-104">SYNTAX</span></span>

### <span data-ttu-id="d05e9-105">ListWebhookByNameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d05e9-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d05e9-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d05e9-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d05e9-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d05e9-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d05e9-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d05e9-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d05e9-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d05e9-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d05e9-110">설명</span><span class="sxs-lookup"><span data-stu-id="d05e9-110">DESCRIPTION</span></span>
<span data-ttu-id="d05e9-111">Get-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리의 지정된 웹후크 또는 컨테이너 레지스트리의 모든 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="d05e9-112">예제</span><span class="sxs-lookup"><span data-stu-id="d05e9-112">EXAMPLES</span></span>

### <span data-ttu-id="d05e9-113">예제 1: 컨테이너 레지스트리의 지정된 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="d05e9-114">컨테이너 레지스트리의 지정된 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="d05e9-115">예제 2: 컨테이너 레지스트리의 모든 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="d05e9-116">컨테이너 레지스트리의 모든 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="d05e9-117">예제 3: 구성 세부 정보를 통해 컨테이너 레지스트리의 지정된 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="d05e9-118">구성 세부 정보를 통해 컨테이너 레지스트리의 지정된 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="d05e9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d05e9-119">PARAMETERS</span></span>

### <span data-ttu-id="d05e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05e9-120">-DefaultProfile</span></span>
<span data-ttu-id="d05e9-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d05e9-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05e9-122">-IncludeConfiguration</span></span>
<span data-ttu-id="d05e9-123">웹후크에 대한 구성 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="d05e9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d05e9-124">-Name</span></span>
<span data-ttu-id="d05e9-125">웹후크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-125">Webhook Name.</span></span>

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

### <span data-ttu-id="d05e9-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="d05e9-126">-Registry</span></span>
<span data-ttu-id="d05e9-127">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="d05e9-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d05e9-128">-RegistryName</span></span>
<span data-ttu-id="d05e9-129">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="d05e9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d05e9-130">-ResourceGroupName</span></span>
<span data-ttu-id="d05e9-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="d05e9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d05e9-132">-ResourceId</span></span>
<span data-ttu-id="d05e9-133">컨테이너 레지스트리 웹후크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d05e9-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="d05e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05e9-134">CommonParameters</span></span>
<span data-ttu-id="d05e9-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d05e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05e9-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d05e9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05e9-137">입력</span><span class="sxs-lookup"><span data-stu-id="d05e9-137">INPUTS</span></span>

### <span data-ttu-id="d05e9-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d05e9-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="d05e9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d05e9-139">System.String</span></span>

## <span data-ttu-id="d05e9-140">출력</span><span class="sxs-lookup"><span data-stu-id="d05e9-140">OUTPUTS</span></span>

### <span data-ttu-id="d05e9-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d05e9-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="d05e9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d05e9-142">NOTES</span></span>

## <span data-ttu-id="d05e9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d05e9-143">RELATED LINKS</span></span>

[<span data-ttu-id="d05e9-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d05e9-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d05e9-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d05e9-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d05e9-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d05e9-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d05e9-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d05e9-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)