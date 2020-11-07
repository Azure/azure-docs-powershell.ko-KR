---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877172"
---
# <span data-ttu-id="7c500-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="7c500-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="7c500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c500-102">SYNOPSIS</span></span>


## <span data-ttu-id="7c500-103">구문과</span><span class="sxs-lookup"><span data-stu-id="7c500-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c500-104">설명은</span><span class="sxs-lookup"><span data-stu-id="7c500-104">DESCRIPTION</span></span>


## <span data-ttu-id="7c500-105">예제의</span><span class="sxs-lookup"><span data-stu-id="7c500-105">EXAMPLES</span></span>

### <span data-ttu-id="7c500-106">예제 1:</span><span class="sxs-lookup"><span data-stu-id="7c500-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="7c500-107">저장소 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c500-107">Update the storage settings.</span></span>

## <span data-ttu-id="7c500-108">변수</span><span class="sxs-lookup"><span data-stu-id="7c500-108">PARAMETERS</span></span>

### <span data-ttu-id="7c500-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c500-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="7c500-110">-Force</span><span class="sxs-lookup"><span data-stu-id="7c500-110">-Force</span></span>


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

### <span data-ttu-id="7c500-111">-위치</span><span class="sxs-lookup"><span data-stu-id="7c500-111">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c500-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="7c500-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c500-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c500-113">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c500-114">-확인</span><span class="sxs-lookup"><span data-stu-id="7c500-114">-Confirm</span></span>
<span data-ttu-id="7c500-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c500-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c500-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c500-116">-WhatIf</span></span>
<span data-ttu-id="7c500-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c500-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c500-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c500-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c500-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c500-119">CommonParameters</span></span>
<span data-ttu-id="7c500-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c500-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c500-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c500-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c500-122">입력</span><span class="sxs-lookup"><span data-stu-id="7c500-122">INPUTS</span></span>

## <span data-ttu-id="7c500-123">출력</span><span class="sxs-lookup"><span data-stu-id="7c500-123">OUTPUTS</span></span>

### <span data-ttu-id="7c500-124">Api201908Preview on. i i m. i a i 설정</span><span class="sxs-lookup"><span data-stu-id="7c500-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="7c500-125">상속자</span><span class="sxs-lookup"><span data-stu-id="7c500-125">NOTES</span></span>

## <span data-ttu-id="7c500-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c500-126">RELATED LINKS</span></span>

