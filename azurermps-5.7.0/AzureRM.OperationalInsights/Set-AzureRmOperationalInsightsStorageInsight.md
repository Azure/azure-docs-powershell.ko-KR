---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 9eb2b145f6a5968f460ba9a9506a4e0956793d01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527976"
---
# <span data-ttu-id="876d2-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="876d2-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="876d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876d2-102">SYNOPSIS</span></span>
<span data-ttu-id="876d2-103">저장소 통찰력을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="876d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="876d2-104">SYNTAX</span></span>

### <span data-ttu-id="876d2-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="876d2-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="876d2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="876d2-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="876d2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="876d2-107">DESCRIPTION</span></span>
<span data-ttu-id="876d2-108">**AzureRmOperationalInsightsStorageInsight** Cmdlet은 저장소 파악의 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="876d2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="876d2-109">EXAMPLES</span></span>

### <span data-ttu-id="876d2-110">예제 1: 이름으로 저장소를 파악 하 여 수정</span><span class="sxs-lookup"><span data-stu-id="876d2-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="876d2-111">이 명령은 저장소에 대 한 MyStorageInsight이 지정 된 테이블을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="876d2-112">예제 2: workspace 개체를 사용 하 여 저장소 통찰력 수정</span><span class="sxs-lookup"><span data-stu-id="876d2-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="876d2-113">첫 번째 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="876d2-114">두 번째 명령은 저장소에 대 한 MyStorageInsight이 지정 된 컨테이너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="876d2-115">변수</span><span class="sxs-lookup"><span data-stu-id="876d2-115">PARAMETERS</span></span>

### <span data-ttu-id="876d2-116">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="876d2-116">-Containers</span></span>
<span data-ttu-id="876d2-117">데이터를 제공 하는 컨테이너의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="876d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876d2-118">-DefaultProfile</span></span>
<span data-ttu-id="876d2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="876d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="876d2-120">-이름</span><span class="sxs-lookup"><span data-stu-id="876d2-120">-Name</span></span>
<span data-ttu-id="876d2-121">저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="876d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="876d2-123">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="876d2-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="876d2-124">-StorageAccountKey</span></span>
<span data-ttu-id="876d2-125">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876d2-126">-테이블</span><span class="sxs-lookup"><span data-stu-id="876d2-126">-Tables</span></span>
<span data-ttu-id="876d2-127">데이터를 포함 하는 테이블의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876d2-128">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="876d2-128">-Workspace</span></span>
<span data-ttu-id="876d2-129">저장소 정보가 포함 된 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="876d2-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="876d2-130">-WorkspaceName</span></span>
<span data-ttu-id="876d2-131">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="876d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876d2-132">CommonParameters</span></span>
<span data-ttu-id="876d2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876d2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876d2-135">입력</span><span class="sxs-lookup"><span data-stu-id="876d2-135">INPUTS</span></span>

### <span data-ttu-id="876d2-136">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="876d2-136">PSWorkspace</span></span>
<span data-ttu-id="876d2-137">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="876d2-137">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="876d2-138">출력</span><span class="sxs-lookup"><span data-stu-id="876d2-138">OUTPUTS</span></span>

### <span data-ttu-id="876d2-139">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="876d2-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="876d2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="876d2-140">NOTES</span></span>

## <span data-ttu-id="876d2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="876d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="876d2-142">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="876d2-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="876d2-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="876d2-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


