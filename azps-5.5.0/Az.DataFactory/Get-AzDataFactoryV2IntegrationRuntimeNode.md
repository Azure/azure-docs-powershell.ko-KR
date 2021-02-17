---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186276"
---
# <span data-ttu-id="395aa-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="395aa-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="395aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395aa-102">SYNOPSIS</span></span>
<span data-ttu-id="395aa-103">통합 런타임 노드 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="395aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="395aa-104">SYNTAX</span></span>

### <span data-ttu-id="395aa-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="395aa-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="395aa-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="395aa-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="395aa-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="395aa-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395aa-108">설명</span><span class="sxs-lookup"><span data-stu-id="395aa-108">DESCRIPTION</span></span>
<span data-ttu-id="395aa-109">**Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet은 통합 런타임 노드의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="395aa-110">예제</span><span class="sxs-lookup"><span data-stu-id="395aa-110">EXAMPLES</span></span>

### <span data-ttu-id="395aa-111">예제 1: 통합 런타임 노드의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="395aa-112">cmdlet은 데이터 팩터리 'test-df-eu2'의 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 'Node_1'라는 노드의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="395aa-113">예제 2: IP 주소와 함께 통합 런타임 노드의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="395aa-114">cmdlet은 IP 주소를 포함하여 데이터 팩터리 'test-df-eu2'의 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 'Node_1'라는 노드의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="395aa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="395aa-115">PARAMETERS</span></span>

### <span data-ttu-id="395aa-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="395aa-116">-DataFactoryName</span></span>
<span data-ttu-id="395aa-117">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-117">The data factory name.</span></span>

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

### <span data-ttu-id="395aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395aa-118">-DefaultProfile</span></span>
<span data-ttu-id="395aa-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="395aa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="395aa-120">-InputObject</span></span>
<span data-ttu-id="395aa-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="395aa-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="395aa-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="395aa-123">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="395aa-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="395aa-124">-IpAddress</span></span>
<span data-ttu-id="395aa-125">통합 런타임 노드의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="395aa-126">-Name</span><span class="sxs-lookup"><span data-stu-id="395aa-126">-Name</span></span>
<span data-ttu-id="395aa-127">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="395aa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395aa-128">-ResourceGroupName</span></span>
<span data-ttu-id="395aa-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-129">The resource group name.</span></span>

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

### <span data-ttu-id="395aa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="395aa-130">-ResourceId</span></span>
<span data-ttu-id="395aa-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="395aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395aa-132">CommonParameters</span></span>
<span data-ttu-id="395aa-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="395aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395aa-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="395aa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395aa-135">입력</span><span class="sxs-lookup"><span data-stu-id="395aa-135">INPUTS</span></span>

### <span data-ttu-id="395aa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="395aa-136">System.String</span></span>

### <span data-ttu-id="395aa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="395aa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="395aa-138">출력</span><span class="sxs-lookup"><span data-stu-id="395aa-138">OUTPUTS</span></span>

### <span data-ttu-id="395aa-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="395aa-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="395aa-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="395aa-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="395aa-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="395aa-141">NOTES</span></span>
<span data-ttu-id="395aa-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="395aa-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="395aa-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="395aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="395aa-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="395aa-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
