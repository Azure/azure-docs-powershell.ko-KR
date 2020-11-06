---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 0e3e82f9dff96fed9e336f95aa44483e85f5ee44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527984"
---
# <span data-ttu-id="8b19e-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="8b19e-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="8b19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b19e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b19e-103">작업 영역 내에서 저장소를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b19e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b19e-104">SYNTAX</span></span>

### <span data-ttu-id="8b19e-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b19e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b19e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8b19e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b19e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8b19e-107">DESCRIPTION</span></span>
<span data-ttu-id="8b19e-108">**새 AzureRmOperationalInsightsStorageInsight** cmdlet은 기존 작업 영역에서 새 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="8b19e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8b19e-109">EXAMPLES</span></span>

### <span data-ttu-id="8b19e-110">예제 1: 이름으로 저장소를 파악 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="8b19e-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="8b19e-111">첫 번째 명령은 Get-AzureRmStorageAccount cmdlet을 사용 하 여 ContosoStorage 이라는 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="8b19e-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 저장소 계정 키를 얻은 다음 $StorageKey 변수에 저장 하 여 $Storage의 저장소 계정을 Get-AzureRmStorageAccountKey cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="8b19e-113">마지막 명령은 MyWorkspace 라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="8b19e-114">이 저장소에서는 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="8b19e-115">예제 2: workspace 개체를 사용 하 여 저장소 통찰력 만들기</span><span class="sxs-lookup"><span data-stu-id="8b19e-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="8b19e-116">첫 번째 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="8b19e-117">두 번째 명령은 Get-AzureRmStorageAccount cmdlet을 사용 하 여 지정 된 저장소 계정을 가져오고이를 $Storage 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="8b19e-118">세 번째 명령은 파이프라인 연산자를 사용 하 여 지정 된 키를 가져와 Get-AzureRmStorageAccountKey cmdlet에 $Storage의 저장소 계정을 전달한 다음 $StorageKey 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="8b19e-119">마지막 명령은 $Workspace에 정의 된 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="8b19e-120">저장소 정보 저장소가 지정 된 저장소 계정 리소스의 WADWindowsEventLogsTable 테이블에 있는 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="8b19e-121">변수</span><span class="sxs-lookup"><span data-stu-id="8b19e-121">PARAMETERS</span></span>

### <span data-ttu-id="8b19e-122">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="8b19e-122">-Containers</span></span>
<span data-ttu-id="8b19e-123">데이터를 포함 하는 컨테이너의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-123">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b19e-124">-DefaultProfile</span></span>
<span data-ttu-id="8b19e-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8b19e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b19e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8b19e-126">-Force</span></span>
<span data-ttu-id="8b19e-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b19e-128">-이름</span><span class="sxs-lookup"><span data-stu-id="8b19e-128">-Name</span></span>
<span data-ttu-id="8b19e-129">저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-129">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b19e-130">-ResourceGroupName</span></span>
<span data-ttu-id="8b19e-131">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b19e-132">-StorageAccountKey</span></span>
<span data-ttu-id="8b19e-133">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-133">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8b19e-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="8b19e-135">저장소 계정의 Azure 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="8b19e-136">이는 Get-AzureRmStorageAccount cmdlet을 실행 하 고 결과의 *Id* 매개 변수에 액세스 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-137">-테이블</span><span class="sxs-lookup"><span data-stu-id="8b19e-137">-Tables</span></span>
<span data-ttu-id="8b19e-138">데이터를 제공 하는 테이블 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-138">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-139">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="8b19e-139">-Workspace</span></span>
<span data-ttu-id="8b19e-140">새 저장소에 대 한 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-140">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b19e-141">-WorkspaceName</span></span>
<span data-ttu-id="8b19e-142">기존 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-142">Specifies the name of an existing workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-143">-확인</span><span class="sxs-lookup"><span data-stu-id="8b19e-143">-Confirm</span></span>
<span data-ttu-id="8b19e-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b19e-145">-WhatIf</span></span>
<span data-ttu-id="8b19e-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b19e-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b19e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b19e-148">CommonParameters</span></span>
<span data-ttu-id="8b19e-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b19e-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b19e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b19e-151">입력</span><span class="sxs-lookup"><span data-stu-id="8b19e-151">INPUTS</span></span>

### <span data-ttu-id="8b19e-152">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b19e-152">PSWorkspace</span></span>
<span data-ttu-id="8b19e-153">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b19e-153">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="8b19e-154">출력</span><span class="sxs-lookup"><span data-stu-id="8b19e-154">OUTPUTS</span></span>

### <span data-ttu-id="8b19e-155">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="8b19e-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="8b19e-156">상속자</span><span class="sxs-lookup"><span data-stu-id="8b19e-156">NOTES</span></span>

## <span data-ttu-id="8b19e-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b19e-157">RELATED LINKS</span></span>

[<span data-ttu-id="8b19e-158">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8b19e-158">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="8b19e-159">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b19e-159">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

