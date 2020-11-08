---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212751"
---
# <span data-ttu-id="6488a-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="6488a-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="6488a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6488a-102">SYNOPSIS</span></span>
<span data-ttu-id="6488a-103">지정 된 작업의 모든 드라이브에 대 한 BitLocker 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="6488a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6488a-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6488a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6488a-105">DESCRIPTION</span></span>
<span data-ttu-id="6488a-106">지정 된 작업의 모든 드라이브에 대 한 BitLocker 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="6488a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6488a-107">EXAMPLES</span></span>

### <span data-ttu-id="6488a-108">예제 1: 지정 된 ImportExport 작업의 모든 BitLocker 키 나열</span><span class="sxs-lookup"><span data-stu-id="6488a-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="6488a-109">이 cmdlet은 지정 된 ImportExport 작업의 모든 BitLocker 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="6488a-110">변수</span><span class="sxs-lookup"><span data-stu-id="6488a-110">PARAMETERS</span></span>

### <span data-ttu-id="6488a-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="6488a-111">-AcceptLanguage</span></span>
<span data-ttu-id="6488a-112">응답의 기본 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6488a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6488a-113">-DefaultProfile</span></span>
<span data-ttu-id="6488a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6488a-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="6488a-115">-JobName</span></span>
<span data-ttu-id="6488a-116">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-116">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6488a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6488a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6488a-118">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6488a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6488a-119">-SubscriptionId</span></span>
<span data-ttu-id="6488a-120">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6488a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6488a-121">CommonParameters</span></span>
<span data-ttu-id="6488a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6488a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6488a-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6488a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6488a-124">입력</span><span class="sxs-lookup"><span data-stu-id="6488a-124">INPUTS</span></span>

## <span data-ttu-id="6488a-125">출력</span><span class="sxs-lookup"><span data-stu-id="6488a-125">OUTPUTS</span></span>

### <span data-ttu-id="6488a-126">Api20161101를 호출 하는. PowerShell. i. i i m.</span><span class="sxs-lookup"><span data-stu-id="6488a-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="6488a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="6488a-127">NOTES</span></span>

<span data-ttu-id="6488a-128">별칭과</span><span class="sxs-lookup"><span data-stu-id="6488a-128">ALIASES</span></span>

## <span data-ttu-id="6488a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6488a-129">RELATED LINKS</span></span>

