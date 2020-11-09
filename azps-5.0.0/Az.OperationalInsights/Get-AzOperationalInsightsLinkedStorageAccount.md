---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308069"
---
# <span data-ttu-id="1c800-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c800-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="1c800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c800-102">SYNOPSIS</span></span>
<span data-ttu-id="1c800-103">연결 된 저장소 계정 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="1c800-103">Get or list linked storage account</span></span>

## <span data-ttu-id="1c800-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c800-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c800-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c800-105">DESCRIPTION</span></span>
<span data-ttu-id="1c800-106">"-DataSourceType"이 지정 되지 않은 경우 연결 된 저장소 계정 가져오기, 연결 된 모든 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="1c800-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="1c800-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1c800-107">EXAMPLES</span></span>

### <span data-ttu-id="1c800-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c800-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="1c800-109">작업 영역에 대 한 연결 된 저장소 accoounts 나열 {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="1c800-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="1c800-110">변수</span><span class="sxs-lookup"><span data-stu-id="1c800-110">PARAMETERS</span></span>

### <span data-ttu-id="1c800-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="1c800-111">-DataSourceType</span></span>
<span data-ttu-id="1c800-112">데이터 원본 유형은 ' CustomLogs ', ' AzureWatson ' 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c800-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c800-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c800-113">-DefaultProfile</span></span>
<span data-ttu-id="1c800-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c800-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c800-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c800-115">-ResourceGroupName</span></span>
<span data-ttu-id="1c800-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c800-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c800-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c800-117">-WorkspaceName</span></span>
<span data-ttu-id="1c800-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c800-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c800-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c800-119">CommonParameters</span></span>
<span data-ttu-id="1c800-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c800-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c800-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1c800-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c800-122">입력</span><span class="sxs-lookup"><span data-stu-id="1c800-122">INPUTS</span></span>

### <span data-ttu-id="1c800-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1c800-123">System.String</span></span>

## <span data-ttu-id="1c800-124">출력</span><span class="sxs-lookup"><span data-stu-id="1c800-124">OUTPUTS</span></span>

### <span data-ttu-id="1c800-125">OperationalInsights. PSLinkedStorageAccountsResource/.</span><span class="sxs-lookup"><span data-stu-id="1c800-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="1c800-126">상속자</span><span class="sxs-lookup"><span data-stu-id="1c800-126">NOTES</span></span>

## <span data-ttu-id="1c800-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c800-127">RELATED LINKS</span></span>