---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5d13fb4c432a0b40fdfd90a5eea55ea44a8b6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528478"
---
# <span data-ttu-id="b1047-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b1047-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="b1047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1047-102">SYNOPSIS</span></span>
<span data-ttu-id="b1047-103">Azure Log Analytics 작업 영역에서 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1047-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1047-104">SYNTAX</span></span>

### <span data-ttu-id="b1047-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1047-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1047-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="b1047-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1047-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="b1047-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1047-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="b1047-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1047-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="b1047-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1047-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b1047-110">DESCRIPTION</span></span>
<span data-ttu-id="b1047-111">**Get-AzureRmOperationalInsightsDataSource** cmdlet은 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="b1047-112">가져올 데이터 원본을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-112">You can specify a data source to get.</span></span>
<span data-ttu-id="b1047-113">데이터 원본의 종류를 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="b1047-114">예제의</span><span class="sxs-lookup"><span data-stu-id="b1047-114">EXAMPLES</span></span>

## <span data-ttu-id="b1047-115">변수</span><span class="sxs-lookup"><span data-stu-id="b1047-115">PARAMETERS</span></span>

### <span data-ttu-id="b1047-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1047-116">-DefaultProfile</span></span>
<span data-ttu-id="b1047-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b1047-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1047-118">-종류</span><span class="sxs-lookup"><span data-stu-id="b1047-118">-Kind</span></span>
<span data-ttu-id="b1047-119">가져올 데이터 원본의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="b1047-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1047-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="b1047-121">AzureActivityLog</span></span> 
- <span data-ttu-id="b1047-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="b1047-122">CustomLog</span></span> 
- <span data-ttu-id="b1047-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="b1047-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="b1047-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="b1047-124">LinuxSyslog</span></span> 
- <span data-ttu-id="b1047-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="b1047-125">WindowsEvent</span></span> 
- <span data-ttu-id="b1047-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="b1047-126">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1047-127">-이름</span><span class="sxs-lookup"><span data-stu-id="b1047-127">-Name</span></span>
<span data-ttu-id="b1047-128">가져올 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-128">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="b1047-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1047-129">-ResourceGroupName</span></span>
<span data-ttu-id="b1047-130">가져올 데이터 원본이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1047-131">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="b1047-131">-Workspace</span></span>
<span data-ttu-id="b1047-132">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-132">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b1047-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1047-133">-WorkspaceName</span></span>
<span data-ttu-id="b1047-134">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1047-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1047-135">CommonParameters</span></span>
<span data-ttu-id="b1047-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1047-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1047-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1047-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1047-138">입력</span><span class="sxs-lookup"><span data-stu-id="b1047-138">INPUTS</span></span>

### <span data-ttu-id="b1047-139">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="b1047-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="b1047-140">매개 변수: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b1047-140">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="b1047-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1047-141">System.String</span></span>

## <span data-ttu-id="b1047-142">출력</span><span class="sxs-lookup"><span data-stu-id="b1047-142">OUTPUTS</span></span>

### <span data-ttu-id="b1047-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b1047-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b1047-144">상속자</span><span class="sxs-lookup"><span data-stu-id="b1047-144">NOTES</span></span>
* <span data-ttu-id="b1047-145">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="b1047-145">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b1047-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1047-146">RELATED LINKS</span></span>

[<span data-ttu-id="b1047-147">제거-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b1047-147">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="b1047-148">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b1047-148">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


