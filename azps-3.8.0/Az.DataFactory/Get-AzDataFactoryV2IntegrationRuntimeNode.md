---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879510"
---
# <span data-ttu-id="8f816-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8f816-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="8f816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f816-102">SYNOPSIS</span></span>
<span data-ttu-id="8f816-103">통합 런타임 노드 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="8f816-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f816-104">SYNTAX</span></span>

### <span data-ttu-id="8f816-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f816-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f816-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f816-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f816-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8f816-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f816-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8f816-108">DESCRIPTION</span></span>
<span data-ttu-id="8f816-109">**AzDataFactoryV2IntegrationRuntimeNode** cmdlet은 통합 런타임 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="8f816-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8f816-110">EXAMPLES</span></span>

### <span data-ttu-id="8f816-111">예제 1: 통합 런타임 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

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

<span data-ttu-id="8f816-112">Cmdlet은 ' selfhost-eu2 ' 데이터 팩터리의 자체 호스팅된 통합 런타임 ' test-ir '의 ' Node_1 ' 노드에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="8f816-113">예제 2: IP 주소와 통합 런타임 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

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

<span data-ttu-id="8f816-114">Cmdlet은 IP 주소를 포함 하 여 데이터 팩터리 ' test-df-eu2 '의 자체 호스팅된 통합 런타임 ' selfhost-ir '의 ' Node_1 ' 노드에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="8f816-115">변수</span><span class="sxs-lookup"><span data-stu-id="8f816-115">PARAMETERS</span></span>

### <span data-ttu-id="8f816-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8f816-116">-DataFactoryName</span></span>
<span data-ttu-id="8f816-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f816-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f816-118">-DefaultProfile</span></span>
<span data-ttu-id="8f816-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f816-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f816-120">-InputObject</span></span>
<span data-ttu-id="8f816-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f816-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8f816-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8f816-123">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f816-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="8f816-124">-IpAddress</span></span>
<span data-ttu-id="8f816-125">통합 런타임 노드의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="8f816-126">-이름</span><span class="sxs-lookup"><span data-stu-id="8f816-126">-Name</span></span>
<span data-ttu-id="8f816-127">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f816-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f816-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f816-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f816-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f816-130">-ResourceId</span></span>
<span data-ttu-id="8f816-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f816-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f816-132">CommonParameters</span></span>
<span data-ttu-id="8f816-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f816-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f816-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f816-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f816-135">입력</span><span class="sxs-lookup"><span data-stu-id="8f816-135">INPUTS</span></span>

### <span data-ttu-id="8f816-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f816-136">System.String</span></span>

### <span data-ttu-id="8f816-137">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="8f816-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8f816-138">출력</span><span class="sxs-lookup"><span data-stu-id="8f816-138">OUTPUTS</span></span>

### <span data-ttu-id="8f816-139">DataFactoryV2. PSManagedIntegrationRuntimeNode/.</span><span class="sxs-lookup"><span data-stu-id="8f816-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="8f816-140">DataFactoryV2. PSSelfHostedIntegrationRuntimeNode/.</span><span class="sxs-lookup"><span data-stu-id="8f816-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="8f816-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8f816-141">NOTES</span></span>
<span data-ttu-id="8f816-142">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="8f816-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8f816-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f816-143">RELATED LINKS</span></span>

[<span data-ttu-id="8f816-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f816-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()