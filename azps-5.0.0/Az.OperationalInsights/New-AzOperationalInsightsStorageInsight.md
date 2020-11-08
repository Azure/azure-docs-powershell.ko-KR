---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217936"
---
# <span data-ttu-id="107c4-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="107c4-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="107c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107c4-102">SYNOPSIS</span></span>
<span data-ttu-id="107c4-103">작업 영역 내에서 저장소를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="107c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="107c4-104">SYNTAX</span></span>

### <span data-ttu-id="107c4-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="107c4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="107c4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="107c4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="107c4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="107c4-107">DESCRIPTION</span></span>
<span data-ttu-id="107c4-108">**새 AzOperationalInsightsStorageInsight** cmdlet은 기존 작업 영역에서 새 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="107c4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="107c4-109">EXAMPLES</span></span>

### <span data-ttu-id="107c4-110">예제 1: 이름으로 저장소를 파악 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="107c4-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="107c4-111">첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 ContosoStorage 이라는 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="107c4-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 저장소 계정 키를 얻은 다음 $StorageKey 변수에 저장 하 여 $Storage의 저장소 계정을 Get-AzStorageAccountKey cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="107c4-113">이 예제에서는 첫 번째 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-113">This example retrieves the first key.</span></span> <span data-ttu-id="107c4-114">다른 항목을 검색 하려면 값 [0] 대신 값 [1]을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="107c4-115">마지막 명령은 MyWorkspace 라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="107c4-116">이 저장소에서는 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="107c4-117">예제 2: workspace 개체를 사용 하 여 저장소 통찰력 만들기</span><span class="sxs-lookup"><span data-stu-id="107c4-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="107c4-118">첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="107c4-119">두 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 지정 된 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="107c4-120">세 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 키를 가져와 Get-AzStorageAccountKey cmdlet에 $Storage의 저장소 계정을 전달한 다음 $StorageKey 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="107c4-121">이 예제에서는 첫 번째 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-121">This example retrieves the first key.</span></span> <span data-ttu-id="107c4-122">다른 항목을 검색 하려면 값 [0] 대신 값 [1]을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="107c4-123">마지막 명령은 $Workspace에 정의 된 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="107c4-124">저장소 정보 저장소가 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="107c4-125">변수</span><span class="sxs-lookup"><span data-stu-id="107c4-125">PARAMETERS</span></span>

### <span data-ttu-id="107c4-126">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="107c4-126">-Containers</span></span>
<span data-ttu-id="107c4-127">데이터를 포함 하는 컨테이너의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="107c4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107c4-128">-DefaultProfile</span></span>
<span data-ttu-id="107c4-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="107c4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="107c4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="107c4-130">-Force</span></span>
<span data-ttu-id="107c4-131">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="107c4-132">-이름</span><span class="sxs-lookup"><span data-stu-id="107c4-132">-Name</span></span>
<span data-ttu-id="107c4-133">저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="107c4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107c4-134">-ResourceGroupName</span></span>
<span data-ttu-id="107c4-135">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="107c4-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="107c4-136">-StorageAccountKey</span></span>
<span data-ttu-id="107c4-137">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="107c4-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="107c4-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="107c4-139">저장소 계정의 Azure 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="107c4-140">이는 Get-AzStorageAccount cmdlet을 실행 하 고 결과의 *Id* 매개 변수에 액세스 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="107c4-141">-테이블</span><span class="sxs-lookup"><span data-stu-id="107c4-141">-Tables</span></span>
<span data-ttu-id="107c4-142">데이터를 제공 하는 테이블 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="107c4-143">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="107c4-143">-Workspace</span></span>
<span data-ttu-id="107c4-144">새 저장소에 대 한 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="107c4-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="107c4-145">-WorkspaceName</span></span>
<span data-ttu-id="107c4-146">기존 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="107c4-147">-확인</span><span class="sxs-lookup"><span data-stu-id="107c4-147">-Confirm</span></span>
<span data-ttu-id="107c4-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107c4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107c4-149">-WhatIf</span></span>
<span data-ttu-id="107c4-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107c4-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107c4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107c4-152">CommonParameters</span></span>
<span data-ttu-id="107c4-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="107c4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107c4-154">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107c4-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107c4-155">입력</span><span class="sxs-lookup"><span data-stu-id="107c4-155">INPUTS</span></span>

### <span data-ttu-id="107c4-156">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="107c4-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="107c4-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="107c4-157">System.String</span></span>

### <span data-ttu-id="107c4-158">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="107c4-158">System.String[]</span></span>

## <span data-ttu-id="107c4-159">출력</span><span class="sxs-lookup"><span data-stu-id="107c4-159">OUTPUTS</span></span>

### <span data-ttu-id="107c4-160">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="107c4-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="107c4-161">상속자</span><span class="sxs-lookup"><span data-stu-id="107c4-161">NOTES</span></span>

## <span data-ttu-id="107c4-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="107c4-162">RELATED LINKS</span></span>

[<span data-ttu-id="107c4-163">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="107c4-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="107c4-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="107c4-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


