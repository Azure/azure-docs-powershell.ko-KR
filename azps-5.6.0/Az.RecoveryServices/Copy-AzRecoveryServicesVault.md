---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960256"
---
# <span data-ttu-id="519ae-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="519ae-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="519ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="519ae-102">SYNOPSIS</span></span>
<span data-ttu-id="519ae-103">한 지역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="519ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="519ae-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="519ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="519ae-105">DESCRIPTION</span></span>
<span data-ttu-id="519ae-106">**Copy-AzRecoveryServicesVault** cmdlet은 한 지역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="519ae-107">현재 자격 증명 모음 수준 데이터 이동만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="519ae-108">예제</span><span class="sxs-lookup"><span data-stu-id="519ae-108">EXAMPLES</span></span>

### <span data-ttu-id="519ae-109">예제 1: Vault1에서 vault2로 데이터 복사</span><span class="sxs-lookup"><span data-stu-id="519ae-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="519ae-110">처음 두 cmdlet은 Recovery Services Vault - 자격 증명 모음1 및 자격 증명 모음2를 각각 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="519ae-111">두 번째 명령은 자격 증명 모음1에서 vault2로 전체 데이터 이동을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="519ae-112">예제 2: 실패한 항목만 사용하여 Vault1에서 vault2로 데이터 복사</span><span class="sxs-lookup"><span data-stu-id="519ae-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="519ae-113">처음 두 cmdlet은 Recovery Services Vault - 자격 증명 모음1 및 자격 증명 모음2를 각각 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="519ae-114">두 번째 명령은 이전 이동 작업에서 실패한 항목만 사용하여 Vault1에서 vault2로 부분 데이터 이동을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="519ae-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="519ae-115">PARAMETERS</span></span>

### <span data-ttu-id="519ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519ae-116">-DefaultProfile</span></span>
<span data-ttu-id="519ae-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="519ae-118">-Force</span><span class="sxs-lookup"><span data-stu-id="519ae-118">-Force</span></span>
<span data-ttu-id="519ae-119">대상 자격 증명 모음 저장소 중복 유형에 대한 확인을 요청하지 않고 데이터 이동 작업(확인 대화 상자 방지)을 강제로 합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="519ae-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="519ae-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="519ae-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="519ae-122">매개 변수를 전환하여 아직 이동되지 않은 원본 자격 증명 모음의 컨테이너에만 데이터 이동을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="519ae-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="519ae-123">-SourceVault</span></span>
<span data-ttu-id="519ae-124">이동할 원본 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-124">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="519ae-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="519ae-125">-TargetVault</span></span>
<span data-ttu-id="519ae-126">데이터를 이동해야 하는 대상 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-126">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="519ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519ae-127">CommonParameters</span></span>
<span data-ttu-id="519ae-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="519ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519ae-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="519ae-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519ae-130">입력</span><span class="sxs-lookup"><span data-stu-id="519ae-130">INPUTS</span></span>

### <span data-ttu-id="519ae-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="519ae-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="519ae-132">출력</span><span class="sxs-lookup"><span data-stu-id="519ae-132">OUTPUTS</span></span>

### <span data-ttu-id="519ae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="519ae-133">System.String</span></span>

## <span data-ttu-id="519ae-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="519ae-134">NOTES</span></span>

## <span data-ttu-id="519ae-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="519ae-135">RELATED LINKS</span></span>
