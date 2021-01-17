---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327179"
---
# <span data-ttu-id="828be-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="828be-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="828be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828be-102">SYNOPSIS</span></span>
<span data-ttu-id="828be-103">작업 영역 내에서 Storage 인사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="828be-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="828be-104">구문</span><span class="sxs-lookup"><span data-stu-id="828be-104">SYNTAX</span></span>

### <span data-ttu-id="828be-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="828be-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="828be-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="828be-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="828be-107">설명</span><span class="sxs-lookup"><span data-stu-id="828be-107">DESCRIPTION</span></span>
<span data-ttu-id="828be-108">**New-AzOperationalInsightsStorageInsight** cmdlet은 기존 작업 영역의 새 Storage Insight를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="828be-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="828be-109">예제</span><span class="sxs-lookup"><span data-stu-id="828be-109">EXAMPLES</span></span>

### <span data-ttu-id="828be-110">예제 1: 이름으로 Storage 인사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="828be-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="828be-111">첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용하여 ContosoStorage라는 저장소 계정을 저장한 다음, $Storage 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="828be-112">두 번째 명령은 파이프라인 연산자를 사용하여 $Storage 저장소 계정 키를 Get-AzStorageAccountKey cmdlet에 저장소 계정을 전달한 다음, $StorageKey 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="828be-113">이 예제에서는 첫 번째 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-113">This example retrieves the first key.</span></span> <span data-ttu-id="828be-114">다른 값을 검색하기 위해 Value[0] 대신 Value[1]을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="828be-115">마지막 명령은 MyWorkspace라는 작업 영역의 MyStorageInsight라는 저장소 인사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="828be-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="828be-116">이 저장소 인사이트는 지정된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블의 데이터를 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="828be-117">예제 2: 작업 영역 개체를 사용하여 Storage Insight 만들기</span><span class="sxs-lookup"><span data-stu-id="828be-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="828be-118">첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음, $Workspace 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="828be-119">두 번째 명령은 Get-AzStorageAccount cmdlet을 사용하여 지정된 저장소 계정을 얻은 다음, $Storage 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="828be-120">세 번째 명령은 파이프라인 연산자를 사용하여 $Storage 저장소 계정을 Get-AzStorageAccountKey cmdlet에 전달한 다음, $StorageKey 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="828be-121">이 예제에서는 첫 번째 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-121">This example retrieves the first key.</span></span> <span data-ttu-id="828be-122">다른 값을 검색하기 위해 Value[0] 대신 Value[1]을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="828be-123">마지막 명령은 MyStorageInsight라는 저장소 인사이트를 이 명령에 정의된 작업 $Workspace.</span><span class="sxs-lookup"><span data-stu-id="828be-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="828be-124">Storage Insight는 지정된 스토리지 계정 리소스의 WADWindowsEventLogsTable 테이블의 데이터를 소비합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="828be-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="828be-125">PARAMETERS</span></span>

### <span data-ttu-id="828be-126">-Containers</span><span class="sxs-lookup"><span data-stu-id="828be-126">-Containers</span></span>
<span data-ttu-id="828be-127">데이터를 포함하는 컨테이너 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="828be-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828be-128">-DefaultProfile</span></span>
<span data-ttu-id="828be-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="828be-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="828be-130">-Force</span><span class="sxs-lookup"><span data-stu-id="828be-130">-Force</span></span>
<span data-ttu-id="828be-131">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="828be-132">-Name</span><span class="sxs-lookup"><span data-stu-id="828be-132">-Name</span></span>
<span data-ttu-id="828be-133">Storage 인사이트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="828be-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828be-134">-ResourceGroupName</span></span>
<span data-ttu-id="828be-135">작업 영역이 포함된 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="828be-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="828be-136">-StorageAccountKey</span></span>
<span data-ttu-id="828be-137">저장소 계정에 대한 액세스 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="828be-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="828be-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="828be-139">저장소 계정의 Azure 리소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="828be-140">이 검색은 Get-AzStorageAccount cmdlet을 실행하고 결과의 *ID* 매개 변수에 액세스하여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="828be-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="828be-141">-Tables</span><span class="sxs-lookup"><span data-stu-id="828be-141">-Tables</span></span>
<span data-ttu-id="828be-142">데이터를 제공하는 테이블 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="828be-143">-Workspace</span><span class="sxs-lookup"><span data-stu-id="828be-143">-Workspace</span></span>
<span data-ttu-id="828be-144">새 Storage 인사이트에 대한 작업 공간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="828be-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="828be-145">-WorkspaceName</span></span>
<span data-ttu-id="828be-146">기존 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="828be-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="828be-147">-Confirm</span></span>
<span data-ttu-id="828be-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="828be-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="828be-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="828be-149">-WhatIf</span></span>
<span data-ttu-id="828be-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="828be-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="828be-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="828be-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="828be-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828be-152">CommonParameters</span></span>
<span data-ttu-id="828be-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="828be-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828be-154">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="828be-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828be-155">입력</span><span class="sxs-lookup"><span data-stu-id="828be-155">INPUTS</span></span>

### <span data-ttu-id="828be-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="828be-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="828be-157">System.String</span><span class="sxs-lookup"><span data-stu-id="828be-157">System.String</span></span>

### <span data-ttu-id="828be-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="828be-158">System.String[]</span></span>

## <span data-ttu-id="828be-159">출력</span><span class="sxs-lookup"><span data-stu-id="828be-159">OUTPUTS</span></span>

### <span data-ttu-id="828be-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="828be-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="828be-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="828be-161">NOTES</span></span>

## <span data-ttu-id="828be-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="828be-162">RELATED LINKS</span></span>

[<span data-ttu-id="828be-163">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="828be-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="828be-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="828be-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


