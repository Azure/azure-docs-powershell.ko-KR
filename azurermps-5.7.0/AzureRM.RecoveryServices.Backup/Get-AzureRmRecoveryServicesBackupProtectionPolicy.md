---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702148"
---
# <span data-ttu-id="77e1d-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="77e1d-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="77e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="77e1d-103">자격 증명 모음에 대 한 백업 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77e1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77e1d-104">SYNTAX</span></span>

### <span data-ttu-id="77e1d-105">NoParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="77e1d-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e1d-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="77e1d-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e1d-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="77e1d-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e1d-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="77e1d-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77e1d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="77e1d-109">DESCRIPTION</span></span>
<span data-ttu-id="77e1d-110">**AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대 한 Azure Backup 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="77e1d-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="77e1d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="77e1d-112">EXAMPLES</span></span>

### <span data-ttu-id="77e1d-113">예제 1: 자격 증명 모음에서 모든 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="77e1d-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="77e1d-114">이 명령은 자격 증명 모음에서 만들어진 모든 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="77e1d-115">예제 2: 특정 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="77e1d-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="77e1d-116">이 명령은 DefaultPolicy 라는 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="77e1d-117">변수</span><span class="sxs-lookup"><span data-stu-id="77e1d-117">PARAMETERS</span></span>

### <span data-ttu-id="77e1d-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="77e1d-118">-BackupManagementType</span></span>
<span data-ttu-id="77e1d-119">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="77e1d-120">현재는 Add-azurevm만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e1d-121">-DefaultProfile</span></span>
<span data-ttu-id="77e1d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e1d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="77e1d-123">-Name</span></span>
<span data-ttu-id="77e1d-124">정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e1d-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="77e1d-125">-WorkloadType</span></span>
<span data-ttu-id="77e1d-126">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-126">Specifies the workload type.</span></span>
<span data-ttu-id="77e1d-127">현재는 Add-azurevm만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e1d-128">CommonParameters</span></span>
<span data-ttu-id="77e1d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e1d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e1d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e1d-131">입력</span><span class="sxs-lookup"><span data-stu-id="77e1d-131">INPUTS</span></span>

### <span data-ttu-id="77e1d-132">않아야</span><span class="sxs-lookup"><span data-stu-id="77e1d-132">None</span></span>
<span data-ttu-id="77e1d-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77e1d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77e1d-134">출력</span><span class="sxs-lookup"><span data-stu-id="77e1d-134">OUTPUTS</span></span>

### <span data-ttu-id="77e1d-135">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="77e1d-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="77e1d-136">System.webserver. IList ' 1 [Microsoft Azure. t e-유틸리티의 모든 이름].</span><span class="sxs-lookup"><span data-stu-id="77e1d-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="77e1d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="77e1d-137">NOTES</span></span>

## <span data-ttu-id="77e1d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77e1d-138">RELATED LINKS</span></span>

[<span data-ttu-id="77e1d-139">새로운 AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="77e1d-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="77e1d-140">제거-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="77e1d-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="77e1d-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="77e1d-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


