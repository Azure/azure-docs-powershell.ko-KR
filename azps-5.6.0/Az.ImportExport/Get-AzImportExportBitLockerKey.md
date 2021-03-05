---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: fefd529b00b88c20b3703e1bcecbbb88c72d52e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963003"
---
# <span data-ttu-id="ecaad-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="ecaad-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="ecaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecaad-102">SYNOPSIS</span></span>
<span data-ttu-id="ecaad-103">지정된 작업의 모든 드라이브에 대한 BitLocker 키를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="ecaad-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecaad-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ecaad-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecaad-105">DESCRIPTION</span></span>
<span data-ttu-id="ecaad-106">지정된 작업의 모든 드라이브에 대한 BitLocker 키를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="ecaad-107">예제</span><span class="sxs-lookup"><span data-stu-id="ecaad-107">EXAMPLES</span></span>

### <span data-ttu-id="ecaad-108">예제 1: 지정된 ImportExport 작업의 모든 BitLocker 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="ecaad-109">이 cmdlet에는 지정된 ImportExport 작업의 모든 BitLocker 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="ecaad-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecaad-110">PARAMETERS</span></span>

### <span data-ttu-id="ecaad-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ecaad-111">-AcceptLanguage</span></span>
<span data-ttu-id="ecaad-112">응답에 대한 기본 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="ecaad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecaad-113">-DefaultProfile</span></span>
<span data-ttu-id="ecaad-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecaad-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="ecaad-115">-JobName</span></span>
<span data-ttu-id="ecaad-116">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="ecaad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecaad-117">-ResourceGroupName</span></span>
<span data-ttu-id="ecaad-118">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="ecaad-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecaad-119">-SubscriptionId</span></span>
<span data-ttu-id="ecaad-120">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="ecaad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecaad-121">CommonParameters</span></span>
<span data-ttu-id="ecaad-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecaad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecaad-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecaad-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecaad-124">입력</span><span class="sxs-lookup"><span data-stu-id="ecaad-124">INPUTS</span></span>

## <span data-ttu-id="ecaad-125">출력</span><span class="sxs-lookup"><span data-stu-id="ecaad-125">OUTPUTS</span></span>

### <span data-ttu-id="ecaad-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="ecaad-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="ecaad-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecaad-127">NOTES</span></span>

<span data-ttu-id="ecaad-128">별칭</span><span class="sxs-lookup"><span data-stu-id="ecaad-128">ALIASES</span></span>

## <span data-ttu-id="ecaad-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecaad-129">RELATED LINKS</span></span>

