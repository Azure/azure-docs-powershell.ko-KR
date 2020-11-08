---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046014"
---
# <span data-ttu-id="d7f55-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7f55-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d7f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f55-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f55-103">사이트 복구에서 복구 계획을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="d7f55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7f55-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7f55-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7f55-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f55-106">**업데이트 AzureSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery의 복구 계획을 업데이트 한 다음 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="d7f55-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7f55-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f55-108">예제 1: 복구 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7f55-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="d7f55-109">이 명령은 지정 된 복구 계획을 업데이트 한 다음 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="d7f55-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7f55-110">PARAMETERS</span></span>

### <span data-ttu-id="d7f55-111">-파일</span><span class="sxs-lookup"><span data-stu-id="d7f55-111">-File</span></span>
<span data-ttu-id="d7f55-112">이 cmdlet이 업데이트 하는 복구 계획의 복구 계획 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f55-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="d7f55-113">-Profile</span></span>
<span data-ttu-id="d7f55-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7f55-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f55-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d7f55-116">-WaitForCompletion</span></span>
<span data-ttu-id="d7f55-117">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d7f55-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f55-118">CommonParameters</span></span>
<span data-ttu-id="d7f55-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f55-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f55-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f55-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f55-121">입력</span><span class="sxs-lookup"><span data-stu-id="d7f55-121">INPUTS</span></span>

## <span data-ttu-id="d7f55-122">출력</span><span class="sxs-lookup"><span data-stu-id="d7f55-122">OUTPUTS</span></span>

## <span data-ttu-id="d7f55-123">상속자</span><span class="sxs-lookup"><span data-stu-id="d7f55-123">NOTES</span></span>

## <span data-ttu-id="d7f55-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7f55-124">RELATED LINKS</span></span>

[<span data-ttu-id="d7f55-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7f55-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d7f55-126">새로운 AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7f55-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d7f55-127">제거-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7f55-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


