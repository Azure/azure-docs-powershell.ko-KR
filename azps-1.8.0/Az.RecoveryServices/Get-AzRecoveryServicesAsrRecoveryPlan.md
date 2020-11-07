---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 8c4bc3598d18042d31e98b37d9fc2c09d45b74d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699725"
---
# <span data-ttu-id="2b32f-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b32f-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2b32f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b32f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b32f-103">복구 계획 또는 복구 서비스 자격 증명 모음의 모든 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="2b32f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b32f-104">SYNTAX</span></span>

### <span data-ttu-id="2b32f-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b32f-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b32f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2b32f-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b32f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b32f-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b32f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b32f-108">DESCRIPTION</span></span>
<span data-ttu-id="2b32f-109">**AzRecoveryServicesAsrRecoveryPlan** cmdlet은 지정 된 복구 계획 또는 복구 서비스 자격 증명 모음의 모든 복구 계획에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="2b32f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b32f-110">EXAMPLES</span></span>

### <span data-ttu-id="2b32f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b32f-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="2b32f-112">지정 된 이름의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="2b32f-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b32f-113">PARAMETERS</span></span>

### <span data-ttu-id="2b32f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b32f-114">-DefaultProfile</span></span>
<span data-ttu-id="2b32f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b32f-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b32f-116">-FriendlyName</span></span>
<span data-ttu-id="2b32f-117">가져올 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b32f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="2b32f-118">-Name</span></span>
<span data-ttu-id="2b32f-119">가져올 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b32f-120">-Path</span><span class="sxs-lookup"><span data-stu-id="2b32f-120">-Path</span></span>
<span data-ttu-id="2b32f-121">이 cmdlet이 복구 계획 json 정의를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="2b32f-122">복구 계획을 수정 하 고 Update-AzRecoveryServicesASRRecoveryPlan cmdlet을 통해 복구 계획을 업데이트 하는 데 사용 되는 json 정의를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b32f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b32f-123">CommonParameters</span></span>
<span data-ttu-id="2b32f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b32f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b32f-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b32f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b32f-126">입력</span><span class="sxs-lookup"><span data-stu-id="2b32f-126">INPUTS</span></span>

### <span data-ttu-id="2b32f-127">않아야</span><span class="sxs-lookup"><span data-stu-id="2b32f-127">None</span></span>

## <span data-ttu-id="2b32f-128">출력</span><span class="sxs-lookup"><span data-stu-id="2b32f-128">OUTPUTS</span></span>

### <span data-ttu-id="2b32f-129">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="2b32f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2b32f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2b32f-130">NOTES</span></span>

## <span data-ttu-id="2b32f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b32f-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b32f-132">새로운 AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b32f-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2b32f-133">제거-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b32f-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2b32f-134">업데이트-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b32f-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
