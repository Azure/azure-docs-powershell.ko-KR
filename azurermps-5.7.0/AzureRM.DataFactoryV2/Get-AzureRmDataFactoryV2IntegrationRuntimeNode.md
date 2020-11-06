---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: cee867b4597237a9593908a110aa3b46850437bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530544"
---
# <span data-ttu-id="94250-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="94250-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="94250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94250-102">SYNOPSIS</span></span>
<span data-ttu-id="94250-103">통합 런타임 노드 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94250-103">Gets an integration runtime node infomation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94250-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94250-104">SYNTAX</span></span>

### <span data-ttu-id="94250-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="94250-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94250-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94250-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94250-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="94250-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94250-108">설명은</span><span class="sxs-lookup"><span data-stu-id="94250-108">DESCRIPTION</span></span>
<span data-ttu-id="94250-109">**AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet은 통합 런타임 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94250-109">The **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="94250-110">예제의</span><span class="sxs-lookup"><span data-stu-id="94250-110">EXAMPLES</span></span>

### <span data-ttu-id="94250-111">예제 1: 통합 런타임 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94250-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="94250-112">Cmdlet은 ' selfhost-eu2 ' 데이터 팩터리의 자체 호스팅된 통합 런타임 ' test-ir '의 ' Node_1 ' 노드에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94250-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="94250-113">예제 2: IP 주소와 통합 런타임 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94250-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="94250-114">Cmdlet은 IP 주소를 포함 하 여 데이터 팩터리 ' test-df-eu2 '의 자체 호스팅된 통합 런타임 ' selfhost-ir '의 ' Node_1 ' 노드에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94250-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="94250-115">변수</span><span class="sxs-lookup"><span data-stu-id="94250-115">PARAMETERS</span></span>

### <span data-ttu-id="94250-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="94250-116">-DataFactoryName</span></span>
<span data-ttu-id="94250-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94250-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94250-118">-DefaultProfile</span></span>
<span data-ttu-id="94250-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94250-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94250-120">-InputObject</span></span>
<span data-ttu-id="94250-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94250-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="94250-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="94250-123">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94250-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="94250-124">-IpAddress</span></span>
<span data-ttu-id="94250-125">통합 런타임 노드의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="94250-126">-이름</span><span class="sxs-lookup"><span data-stu-id="94250-126">-Name</span></span>
<span data-ttu-id="94250-127">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-127">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94250-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94250-128">-ResourceGroupName</span></span>
<span data-ttu-id="94250-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94250-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94250-130">-ResourceId</span></span>
<span data-ttu-id="94250-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94250-131">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94250-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94250-132">CommonParameters</span></span>
<span data-ttu-id="94250-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94250-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94250-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94250-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94250-135">입력</span><span class="sxs-lookup"><span data-stu-id="94250-135">INPUTS</span></span>

### <span data-ttu-id="94250-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94250-136">System.String</span></span>
<span data-ttu-id="94250-137">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="94250-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="94250-138">출력</span><span class="sxs-lookup"><span data-stu-id="94250-138">OUTPUTS</span></span>

### <span data-ttu-id="94250-139">DataFactoryV2. PSManagedIntegrationRuntimeNode/.</span><span class="sxs-lookup"><span data-stu-id="94250-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>
<span data-ttu-id="94250-140">DataFactoryV2. PSSelfHostedIntegrationRuntimeNode/.</span><span class="sxs-lookup"><span data-stu-id="94250-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="94250-141">상속자</span><span class="sxs-lookup"><span data-stu-id="94250-141">NOTES</span></span>
<span data-ttu-id="94250-142">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="94250-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="94250-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94250-143">RELATED LINKS</span></span>

[<span data-ttu-id="94250-144">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="94250-144">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
