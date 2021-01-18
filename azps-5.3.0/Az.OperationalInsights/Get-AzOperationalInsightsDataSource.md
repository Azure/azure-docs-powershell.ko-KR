---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496400"
---
# <span data-ttu-id="914d9-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="914d9-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="914d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="914d9-102">SYNOPSIS</span></span>
<span data-ttu-id="914d9-103">Azure Log Analytics 작업 영역 아래에서 데이터 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="914d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="914d9-104">SYNTAX</span></span>

### <span data-ttu-id="914d9-105">ByWorkspaceNameByKind(기본값)</span><span class="sxs-lookup"><span data-stu-id="914d9-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="914d9-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="914d9-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="914d9-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="914d9-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="914d9-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="914d9-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="914d9-109">설명</span><span class="sxs-lookup"><span data-stu-id="914d9-109">DESCRIPTION</span></span>
<span data-ttu-id="914d9-110">**Get-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="914d9-111">사용할 데이터 원본을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-111">You can specify a data source to get.</span></span>
<span data-ttu-id="914d9-112">데이터 원본의 종류에 따라 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="914d9-113">예제</span><span class="sxs-lookup"><span data-stu-id="914d9-113">EXAMPLES</span></span>

## <span data-ttu-id="914d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="914d9-114">PARAMETERS</span></span>

### <span data-ttu-id="914d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914d9-115">-DefaultProfile</span></span>
<span data-ttu-id="914d9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="914d9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="914d9-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="914d9-117">-Kind</span></span>
<span data-ttu-id="914d9-118">얻을 데이터 원본의 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="914d9-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="914d9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="914d9-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="914d9-120">AzureActivityLog</span></span> 
- <span data-ttu-id="914d9-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="914d9-121">CustomLog</span></span> 
- <span data-ttu-id="914d9-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="914d9-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="914d9-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="914d9-123">LinuxSyslog</span></span> 
- <span data-ttu-id="914d9-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="914d9-124">WindowsEvent</span></span> 
- <span data-ttu-id="914d9-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="914d9-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="914d9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="914d9-126">-Name</span></span>
<span data-ttu-id="914d9-127">얻을 데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="914d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="914d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="914d9-129">얻을 데이터 원본이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="914d9-130">-Workspace</span><span class="sxs-lookup"><span data-stu-id="914d9-130">-Workspace</span></span>
<span data-ttu-id="914d9-131">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="914d9-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="914d9-132">-WorkspaceName</span></span>
<span data-ttu-id="914d9-133">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="914d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914d9-134">CommonParameters</span></span>
<span data-ttu-id="914d9-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="914d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914d9-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="914d9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914d9-137">입력</span><span class="sxs-lookup"><span data-stu-id="914d9-137">INPUTS</span></span>

### <span data-ttu-id="914d9-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="914d9-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="914d9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="914d9-139">System.String</span></span>

## <span data-ttu-id="914d9-140">출력</span><span class="sxs-lookup"><span data-stu-id="914d9-140">OUTPUTS</span></span>

### <span data-ttu-id="914d9-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="914d9-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="914d9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="914d9-142">NOTES</span></span>
* <span data-ttu-id="914d9-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="914d9-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="914d9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="914d9-144">RELATED LINKS</span></span>

[<span data-ttu-id="914d9-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="914d9-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="914d9-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="914d9-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


