---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045976"
---
# <span data-ttu-id="7ba47-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7ba47-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="7ba47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba47-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba47-103">사이트 복구에 사이트 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="7ba47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ba47-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ba47-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7ba47-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba47-106">**새 AzureSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery에서 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="7ba47-107">복구 계획은 장애 조치와 복구를 위해 그룹의 가상 컴퓨터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="7ba47-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7ba47-108">EXAMPLES</span></span>

### <span data-ttu-id="7ba47-109">예제 1: 사이트 복구 자격 증명 모음에 복구 계획 추가</span><span class="sxs-lookup"><span data-stu-id="7ba47-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="7ba47-110">이 명령은 RecoveryPlan.xml 라는 복구 계획을 Azure Site Recovery 자격 증명 모음에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7ba47-111">변수</span><span class="sxs-lookup"><span data-stu-id="7ba47-111">PARAMETERS</span></span>

### <span data-ttu-id="7ba47-112">-파일</span><span class="sxs-lookup"><span data-stu-id="7ba47-112">-File</span></span>
<span data-ttu-id="7ba47-113">복구 계획 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="7ba47-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="7ba47-114">-Profile</span></span>
<span data-ttu-id="7ba47-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ba47-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ba47-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7ba47-117">-WaitForCompletion</span></span>
<span data-ttu-id="7ba47-118">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7ba47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba47-119">CommonParameters</span></span>
<span data-ttu-id="7ba47-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ba47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba47-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba47-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba47-122">입력</span><span class="sxs-lookup"><span data-stu-id="7ba47-122">INPUTS</span></span>

## <span data-ttu-id="7ba47-123">출력</span><span class="sxs-lookup"><span data-stu-id="7ba47-123">OUTPUTS</span></span>

## <span data-ttu-id="7ba47-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7ba47-124">NOTES</span></span>

## <span data-ttu-id="7ba47-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ba47-125">RELATED LINKS</span></span>

[<span data-ttu-id="7ba47-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7ba47-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7ba47-127">제거-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7ba47-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7ba47-128">업데이트-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7ba47-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


