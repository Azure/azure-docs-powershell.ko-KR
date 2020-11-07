---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: f291eedade1a1a243f22dc618ffcc538a9158de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699862"
---
# <span data-ttu-id="5caf3-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5caf3-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5caf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5caf3-102">SYNOPSIS</span></span>
<span data-ttu-id="5caf3-103">Azure Log Analytics 작업 영역에서 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="5caf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5caf3-104">SYNTAX</span></span>

### <span data-ttu-id="5caf3-105">ByWorkspaceNameByKind (기본값)</span><span class="sxs-lookup"><span data-stu-id="5caf3-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5caf3-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="5caf3-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5caf3-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="5caf3-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5caf3-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="5caf3-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5caf3-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5caf3-109">DESCRIPTION</span></span>
<span data-ttu-id="5caf3-110">**Get-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="5caf3-111">가져올 데이터 원본을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-111">You can specify a data source to get.</span></span>
<span data-ttu-id="5caf3-112">데이터 원본의 종류를 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="5caf3-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5caf3-113">EXAMPLES</span></span>

## <span data-ttu-id="5caf3-114">변수</span><span class="sxs-lookup"><span data-stu-id="5caf3-114">PARAMETERS</span></span>

### <span data-ttu-id="5caf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5caf3-115">-DefaultProfile</span></span>
<span data-ttu-id="5caf3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5caf3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5caf3-117">-종류</span><span class="sxs-lookup"><span data-stu-id="5caf3-117">-Kind</span></span>
<span data-ttu-id="5caf3-118">가져올 데이터 원본의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="5caf3-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5caf3-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="5caf3-120">AzureActivityLog</span></span> 
- <span data-ttu-id="5caf3-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="5caf3-121">CustomLog</span></span> 
- <span data-ttu-id="5caf3-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="5caf3-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="5caf3-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="5caf3-123">LinuxSyslog</span></span> 
- <span data-ttu-id="5caf3-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="5caf3-124">WindowsEvent</span></span> 
- <span data-ttu-id="5caf3-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="5caf3-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="5caf3-126">-이름</span><span class="sxs-lookup"><span data-stu-id="5caf3-126">-Name</span></span>
<span data-ttu-id="5caf3-127">가져올 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="5caf3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5caf3-128">-ResourceGroupName</span></span>
<span data-ttu-id="5caf3-129">가져올 데이터 원본이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="5caf3-130">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="5caf3-130">-Workspace</span></span>
<span data-ttu-id="5caf3-131">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5caf3-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5caf3-132">-WorkspaceName</span></span>
<span data-ttu-id="5caf3-133">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5caf3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5caf3-134">CommonParameters</span></span>
<span data-ttu-id="5caf3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caf3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5caf3-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5caf3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5caf3-137">입력</span><span class="sxs-lookup"><span data-stu-id="5caf3-137">INPUTS</span></span>

### <span data-ttu-id="5caf3-138">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="5caf3-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5caf3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5caf3-139">System.String</span></span>

## <span data-ttu-id="5caf3-140">출력</span><span class="sxs-lookup"><span data-stu-id="5caf3-140">OUTPUTS</span></span>

### <span data-ttu-id="5caf3-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5caf3-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5caf3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5caf3-142">NOTES</span></span>
* <span data-ttu-id="5caf3-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="5caf3-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5caf3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5caf3-144">RELATED LINKS</span></span>

[<span data-ttu-id="5caf3-145">제거-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5caf3-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="5caf3-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5caf3-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)

