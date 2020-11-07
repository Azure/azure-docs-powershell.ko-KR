---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: e4f966d542110f96672857c2222d44ae03d331ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880174"
---
# <span data-ttu-id="c4705-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c4705-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="c4705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4705-102">SYNOPSIS</span></span>
<span data-ttu-id="c4705-103">작업 영역 내에서 저장소를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="c4705-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4705-104">SYNTAX</span></span>

### <span data-ttu-id="c4705-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c4705-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4705-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c4705-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4705-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c4705-107">DESCRIPTION</span></span>
<span data-ttu-id="c4705-108">**새 AzOperationalInsightsStorageInsight** cmdlet은 기존 작업 영역에서 새 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="c4705-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c4705-109">EXAMPLES</span></span>

### <span data-ttu-id="c4705-110">예제 1: 이름으로 저장소를 파악 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="c4705-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c4705-111">첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 ContosoStorage 이라는 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="c4705-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 저장소 계정 키를 얻은 다음 $StorageKey 변수에 저장 하 여 $Storage의 저장소 계정을 Get-AzStorageAccountKey cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="c4705-113">마지막 명령은 MyWorkspace 라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="c4705-114">이 저장소에서는 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="c4705-115">예제 2: workspace 개체를 사용 하 여 저장소 통찰력 만들기</span><span class="sxs-lookup"><span data-stu-id="c4705-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c4705-116">첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-116">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="c4705-117">두 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 지정 된 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-117">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="c4705-118">세 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 키를 가져와 Get-AzStorageAccountKey cmdlet에 $Storage의 저장소 계정을 전달한 다음 $StorageKey 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-118">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="c4705-119">마지막 명령은 $Workspace에 정의 된 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="c4705-120">저장소 정보 저장소가 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="c4705-121">변수</span><span class="sxs-lookup"><span data-stu-id="c4705-121">PARAMETERS</span></span>

### <span data-ttu-id="c4705-122">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="c4705-122">-Containers</span></span>
<span data-ttu-id="c4705-123">데이터를 포함 하는 컨테이너의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-123">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4705-124">-DefaultProfile</span></span>
<span data-ttu-id="c4705-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c4705-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4705-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c4705-126">-Force</span></span>
<span data-ttu-id="c4705-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4705-128">-이름</span><span class="sxs-lookup"><span data-stu-id="c4705-128">-Name</span></span>
<span data-ttu-id="c4705-129">저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-129">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4705-130">-ResourceGroupName</span></span>
<span data-ttu-id="c4705-131">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4705-132">-StorageAccountKey</span></span>
<span data-ttu-id="c4705-133">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-133">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c4705-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="c4705-135">저장소 계정의 Azure 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="c4705-136">이는 Get-AzStorageAccount cmdlet을 실행 하 고 결과의 *Id* 매개 변수에 액세스 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-136">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-137">-테이블</span><span class="sxs-lookup"><span data-stu-id="c4705-137">-Tables</span></span>
<span data-ttu-id="c4705-138">데이터를 제공 하는 테이블 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-138">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-139">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="c4705-139">-Workspace</span></span>
<span data-ttu-id="c4705-140">새 저장소에 대 한 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-140">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c4705-141">-WorkspaceName</span></span>
<span data-ttu-id="c4705-142">기존 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-142">Specifies the name of an existing workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-143">-확인</span><span class="sxs-lookup"><span data-stu-id="c4705-143">-Confirm</span></span>
<span data-ttu-id="c4705-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4705-145">-WhatIf</span></span>
<span data-ttu-id="c4705-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4705-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4705-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4705-148">CommonParameters</span></span>
<span data-ttu-id="c4705-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4705-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4705-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4705-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4705-151">입력</span><span class="sxs-lookup"><span data-stu-id="c4705-151">INPUTS</span></span>

### <span data-ttu-id="c4705-152">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="c4705-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c4705-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4705-153">System.String</span></span>

### <span data-ttu-id="c4705-154">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="c4705-154">System.String[]</span></span>

## <span data-ttu-id="c4705-155">출력</span><span class="sxs-lookup"><span data-stu-id="c4705-155">OUTPUTS</span></span>

### <span data-ttu-id="c4705-156">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="c4705-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="c4705-157">상속자</span><span class="sxs-lookup"><span data-stu-id="c4705-157">NOTES</span></span>

## <span data-ttu-id="c4705-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4705-158">RELATED LINKS</span></span>

[<span data-ttu-id="c4705-159">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4705-159">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c4705-160">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c4705-160">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


