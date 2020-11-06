---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 61846456cfbff2dcbdaffba8c73a9bada87f07dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533931"
---
# <span data-ttu-id="91b21-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="91b21-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="91b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b21-102">SYNOPSIS</span></span>
<span data-ttu-id="91b21-103">Azure Log Analytics 작업 영역에서 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91b21-104">SYNTAX</span></span>

### <span data-ttu-id="91b21-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="91b21-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b21-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="91b21-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b21-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="91b21-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b21-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="91b21-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b21-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="91b21-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b21-110">설명은</span><span class="sxs-lookup"><span data-stu-id="91b21-110">DESCRIPTION</span></span>
<span data-ttu-id="91b21-111">**Get-AzureRmOperationalInsightsDataSource** cmdlet은 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="91b21-112">가져올 데이터 원본을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-112">You can specify a data source to get.</span></span>
<span data-ttu-id="91b21-113">데이터 원본의 종류를 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="91b21-114">예제의</span><span class="sxs-lookup"><span data-stu-id="91b21-114">EXAMPLES</span></span>

## <span data-ttu-id="91b21-115">변수</span><span class="sxs-lookup"><span data-stu-id="91b21-115">PARAMETERS</span></span>

### <span data-ttu-id="91b21-116">-종류</span><span class="sxs-lookup"><span data-stu-id="91b21-116">-Kind</span></span>
<span data-ttu-id="91b21-117">가져올 데이터 원본의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-117">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="91b21-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91b21-119">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="91b21-119">AzureActivityLog</span></span> 
- <span data-ttu-id="91b21-120">CustomLog</span><span class="sxs-lookup"><span data-stu-id="91b21-120">CustomLog</span></span> 
- <span data-ttu-id="91b21-121">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="91b21-121">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="91b21-122">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="91b21-122">LinuxSyslog</span></span> 
- <span data-ttu-id="91b21-123">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="91b21-123">WindowsEvent</span></span> 
- <span data-ttu-id="91b21-124">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="91b21-124">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

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
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b21-125">-이름</span><span class="sxs-lookup"><span data-stu-id="91b21-125">-Name</span></span>
<span data-ttu-id="91b21-126">가져올 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-126">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="91b21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b21-127">-ResourceGroupName</span></span>
<span data-ttu-id="91b21-128">가져올 데이터 원본이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-128">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="91b21-129">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="91b21-129">-Workspace</span></span>
<span data-ttu-id="91b21-130">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="91b21-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="91b21-131">-WorkspaceName</span></span>
<span data-ttu-id="91b21-132">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="91b21-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b21-133">-DefaultProfile</span></span>
<span data-ttu-id="91b21-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b21-135">CommonParameters</span></span>
<span data-ttu-id="91b21-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b21-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b21-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b21-138">입력</span><span class="sxs-lookup"><span data-stu-id="91b21-138">INPUTS</span></span>

### <span data-ttu-id="91b21-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="91b21-139">PSWorkspace</span></span>
<span data-ttu-id="91b21-140">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="91b21-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="91b21-141">PSWorkspace</span></span>
<span data-ttu-id="91b21-142">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b21-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="91b21-143">출력</span><span class="sxs-lookup"><span data-stu-id="91b21-143">OUTPUTS</span></span>

### <span data-ttu-id="91b21-144">System.webserver. List ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="91b21-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="91b21-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="91b21-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="91b21-146">상속자</span><span class="sxs-lookup"><span data-stu-id="91b21-146">NOTES</span></span>
* <span data-ttu-id="91b21-147">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="91b21-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="91b21-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91b21-148">RELATED LINKS</span></span>

[<span data-ttu-id="91b21-149">제거-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="91b21-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="91b21-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="91b21-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


