---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: e456ae28bec5f5421dad9c58bc5afb58c4d0d250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202108"
---
# <span data-ttu-id="ae895-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ae895-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ae895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae895-102">SYNOPSIS</span></span>
<span data-ttu-id="ae895-103">한 지역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="ae895-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae895-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="ae895-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae895-105">DESCRIPTION</span></span>
<span data-ttu-id="ae895-106">**Copy-AzRecoveryServicesVault** cmdlet은 한 지역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="ae895-107">현재는 자격 증명 모음 수준 데이터 이동만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="ae895-108">예제</span><span class="sxs-lookup"><span data-stu-id="ae895-108">EXAMPLES</span></span>

### <span data-ttu-id="ae895-109">예제 1: vault1에서 vault2로 데이터 복사</span><span class="sxs-lookup"><span data-stu-id="ae895-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="ae895-110">처음 두 cmdlet은 Recovery Services 자격 증명 모음(vault1 및 vault2)을 각각 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="ae895-111">두 번째 명령은 vault1에서 vault2로 전체 데이터 이동을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="ae895-112">예제 2: 실패한 항목만 있는 vault1에서 vault2로 데이터 복사</span><span class="sxs-lookup"><span data-stu-id="ae895-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="ae895-113">처음 두 cmdlet은 Recovery Services 자격 증명 모음(vault1 및 vault2)을 각각 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="ae895-114">두 번째 명령은 이전 이동 작업에서 실패한 항목만 사용하여 vault1에서 vault2로 부분 데이터 이동을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="ae895-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae895-115">PARAMETERS</span></span>

### <span data-ttu-id="ae895-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae895-116">-DefaultProfile</span></span>
<span data-ttu-id="ae895-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae895-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ae895-118">-Force</span></span>
<span data-ttu-id="ae895-119">대상 자격 증명 모음 저장소 중복 유형에 대한 확인을 요청하지 않고 데이터 이동 작업(확인 대화 상자 방지)을 강제합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="ae895-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="ae895-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="ae895-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="ae895-122">매개 변수를 전환하여 아직 이동되지 않은 원본 자격 증명 모음의 컨테이너에 대한 데이터 이동만 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="ae895-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="ae895-123">-SourceVault</span></span>
<span data-ttu-id="ae895-124">이동할 원본 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae895-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="ae895-125">-TargetVault</span></span>
<span data-ttu-id="ae895-126">데이터를 이동해야 하는 대상 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae895-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae895-127">CommonParameters</span></span>
<span data-ttu-id="ae895-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae895-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae895-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae895-130">입력</span><span class="sxs-lookup"><span data-stu-id="ae895-130">INPUTS</span></span>

### <span data-ttu-id="ae895-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="ae895-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ae895-132">출력</span><span class="sxs-lookup"><span data-stu-id="ae895-132">OUTPUTS</span></span>

### <span data-ttu-id="ae895-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ae895-133">System.String</span></span>

## <span data-ttu-id="ae895-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae895-134">NOTES</span></span>

## <span data-ttu-id="ae895-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae895-135">RELATED LINKS</span></span>
