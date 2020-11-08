---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045583"
---
# <span data-ttu-id="e38de-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="e38de-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="e38de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38de-102">SYNOPSIS</span></span>
<span data-ttu-id="e38de-103">Azure Site Recovery 계획을 XML 형식으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="e38de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e38de-104">SYNTAX</span></span>

### <span data-ttu-id="e38de-105">ByRPObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="e38de-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e38de-106">ById</span><span class="sxs-lookup"><span data-stu-id="e38de-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e38de-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e38de-107">DESCRIPTION</span></span>
<span data-ttu-id="e38de-108">**AzureSiteRecoveryRecoveryPlanFile** Cmdlet은 Azure Site Recovery 계획을 XML 형식으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="e38de-109">이 파일을 사용 하 여 복구 계획을 업데이트 한 다음 사이트 복구 서버로 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="e38de-110">복구 계획은 장애 조치와 복구를 위해 그룹의 가상 컴퓨터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="e38de-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e38de-111">EXAMPLES</span></span>

### <span data-ttu-id="e38de-112">예제 1: 복구 계획 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="e38de-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="e38de-113">이 명령은 **AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 하 여 복구 계획을 얻은 다음 $RecoveryPlan 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="e38de-114">두 번째 명령은 **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet을 사용 하 여 $RecoveryPlan에서 사이트 복구 계획 XML 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="e38de-115">명령은 지정 된 경로에 XML 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="e38de-116">변수</span><span class="sxs-lookup"><span data-stu-id="e38de-116">PARAMETERS</span></span>

### <span data-ttu-id="e38de-117">-Id</span><span class="sxs-lookup"><span data-stu-id="e38de-117">-Id</span></span>
<span data-ttu-id="e38de-118">가져올 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-118">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38de-119">-Path</span><span class="sxs-lookup"><span data-stu-id="e38de-119">-Path</span></span>
<span data-ttu-id="e38de-120">복구 계획 XML 파일을 저장할 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="e38de-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="e38de-121">-Profile</span></span>
<span data-ttu-id="e38de-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e38de-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e38de-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e38de-124">-RecoveryPlan</span></span>
<span data-ttu-id="e38de-125">복구 계획을 가져올 **Asrrecoveryplan** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="e38de-126">**Asrrecoveryplan** 개체를 얻으려면 **Get-AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38de-127">CommonParameters</span></span>
<span data-ttu-id="e38de-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38de-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38de-130">입력</span><span class="sxs-lookup"><span data-stu-id="e38de-130">INPUTS</span></span>

## <span data-ttu-id="e38de-131">출력</span><span class="sxs-lookup"><span data-stu-id="e38de-131">OUTPUTS</span></span>

## <span data-ttu-id="e38de-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e38de-132">NOTES</span></span>

## <span data-ttu-id="e38de-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e38de-133">RELATED LINKS</span></span>

[<span data-ttu-id="e38de-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e38de-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


