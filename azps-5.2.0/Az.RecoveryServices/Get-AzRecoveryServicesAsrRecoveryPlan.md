---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352634"
---
# <span data-ttu-id="c255f-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c255f-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="c255f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c255f-102">SYNOPSIS</span></span>
<span data-ttu-id="c255f-103">Recovery Services 자격 증명 모음에서 복구 계획 또는 모든 복구 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="c255f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c255f-104">SYNTAX</span></span>

### <span data-ttu-id="c255f-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="c255f-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c255f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c255f-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c255f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c255f-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c255f-108">설명</span><span class="sxs-lookup"><span data-stu-id="c255f-108">DESCRIPTION</span></span>
<span data-ttu-id="c255f-109">**Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet은 Recovery Services 자격 증명 모음에서 지정된 복구 계획 또는 모든 복구 계획의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="c255f-110">예제</span><span class="sxs-lookup"><span data-stu-id="c255f-110">EXAMPLES</span></span>

### <span data-ttu-id="c255f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c255f-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="c255f-112">지정된 이름으로 복구 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="c255f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c255f-113">PARAMETERS</span></span>

### <span data-ttu-id="c255f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c255f-114">-DefaultProfile</span></span>
<span data-ttu-id="c255f-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c255f-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c255f-116">-FriendlyName</span></span>
<span data-ttu-id="c255f-117">얻을 복구 계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="c255f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c255f-118">-Name</span></span>
<span data-ttu-id="c255f-119">얻을 복구 계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="c255f-120">-Path</span><span class="sxs-lookup"><span data-stu-id="c255f-120">-Path</span></span>
<span data-ttu-id="c255f-121">이 cmdlet이 복구 계획 json 정의를 저장할 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="c255f-122">json 정의를 편집하여 복구 계획을 수정하고 Update-AzRecoveryServicesASRRecoveryPlan cmdlet을 통해 복구 계획을 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="c255f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c255f-123">CommonParameters</span></span>
<span data-ttu-id="c255f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c255f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c255f-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c255f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c255f-126">입력</span><span class="sxs-lookup"><span data-stu-id="c255f-126">INPUTS</span></span>

### <span data-ttu-id="c255f-127">없음</span><span class="sxs-lookup"><span data-stu-id="c255f-127">None</span></span>

## <span data-ttu-id="c255f-128">출력</span><span class="sxs-lookup"><span data-stu-id="c255f-128">OUTPUTS</span></span>

### <span data-ttu-id="c255f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c255f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c255f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c255f-130">NOTES</span></span>

## <span data-ttu-id="c255f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c255f-131">RELATED LINKS</span></span>

[<span data-ttu-id="c255f-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c255f-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c255f-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c255f-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c255f-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c255f-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
