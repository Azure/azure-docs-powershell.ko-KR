---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529004"
---
# <span data-ttu-id="02e65-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02e65-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="02e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02e65-102">SYNOPSIS</span></span>
<span data-ttu-id="02e65-103">컨테이너 레지스트리 webhook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02e65-104">SYNTAX</span></span>

### <span data-ttu-id="02e65-105">ListWebhookByNameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="02e65-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02e65-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="02e65-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02e65-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02e65-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02e65-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02e65-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02e65-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02e65-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02e65-110">설명은</span><span class="sxs-lookup"><span data-stu-id="02e65-110">DESCRIPTION</span></span>
<span data-ttu-id="02e65-111">Get-AzureRmContainerRegistryWebhook cmdlet은 컨테이너 레지스트리의 지정 된 webhook 또는 컨테이너 레지스트리의 모든 webhooks 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="02e65-112">예제의</span><span class="sxs-lookup"><span data-stu-id="02e65-112">EXAMPLES</span></span>

### <span data-ttu-id="02e65-113">예제 1: 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="02e65-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="02e65-114">컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="02e65-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="02e65-115">예제 2: 컨테이너 레지스트리의 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="02e65-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="02e65-116">컨테이너 레지스트리의 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="02e65-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="02e65-117">예제 3: 구성 세부 정보를 사용 하 여 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="02e65-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="02e65-118">구성 세부 정보를 사용 하 여 컨테이너 레지스트리의 지정 된 webhook 가져오기</span><span class="sxs-lookup"><span data-stu-id="02e65-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="02e65-119">변수</span><span class="sxs-lookup"><span data-stu-id="02e65-119">PARAMETERS</span></span>

### <span data-ttu-id="02e65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e65-120">-DefaultProfile</span></span>
<span data-ttu-id="02e65-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02e65-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="02e65-122">-IncludeConfiguration</span></span>
<span data-ttu-id="02e65-123">Webhook에 대 한 구성 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e65-124">-이름</span><span class="sxs-lookup"><span data-stu-id="02e65-124">-Name</span></span>
<span data-ttu-id="02e65-125">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="02e65-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e65-126">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="02e65-126">-Registry</span></span>
<span data-ttu-id="02e65-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e65-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="02e65-128">-RegistryName</span></span>
<span data-ttu-id="02e65-129">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e65-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e65-130">-ResourceGroupName</span></span>
<span data-ttu-id="02e65-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e65-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02e65-132">-ResourceId</span></span>
<span data-ttu-id="02e65-133">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="02e65-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="02e65-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e65-134">CommonParameters</span></span>
<span data-ttu-id="02e65-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02e65-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e65-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e65-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e65-137">입력</span><span class="sxs-lookup"><span data-stu-id="02e65-137">INPUTS</span></span>

### <span data-ttu-id="02e65-138">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="02e65-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="02e65-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02e65-139">System.String</span></span>

## <span data-ttu-id="02e65-140">출력</span><span class="sxs-lookup"><span data-stu-id="02e65-140">OUTPUTS</span></span>

### <span data-ttu-id="02e65-141">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02e65-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="02e65-142">System.webserver. IList ' 1 [[ContainerRegistry PSContainerRegistryWebhook, Microsoft azure. ContainerRegistry, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="02e65-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="02e65-143">상속자</span><span class="sxs-lookup"><span data-stu-id="02e65-143">NOTES</span></span>

## <span data-ttu-id="02e65-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02e65-144">RELATED LINKS</span></span>

[<span data-ttu-id="02e65-145">새로운 AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02e65-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="02e65-146">업데이트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02e65-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="02e65-147">제거-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02e65-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="02e65-148">테스트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02e65-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
