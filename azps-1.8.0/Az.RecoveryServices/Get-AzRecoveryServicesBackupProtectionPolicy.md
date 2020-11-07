---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 295cb5bad09584c16e1217e68d3fc80c5ebf8598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699698"
---
# <span data-ttu-id="3c75e-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c75e-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="3c75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c75e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c75e-103">자격 증명 모음에 대 한 백업 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="3c75e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c75e-104">SYNTAX</span></span>

### <span data-ttu-id="3c75e-105">NoParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3c75e-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c75e-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="3c75e-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c75e-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="3c75e-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c75e-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="3c75e-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c75e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3c75e-109">DESCRIPTION</span></span>
<span data-ttu-id="3c75e-110">**AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대 한 Azure Backup 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="3c75e-111">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3c75e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3c75e-112">EXAMPLES</span></span>

### <span data-ttu-id="3c75e-113">예제 1: 자격 증명 모음에서 모든 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="3c75e-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="3c75e-114">이 명령은 자격 증명 모음에서 만들어진 모든 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="3c75e-115">예제 2: 특정 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="3c75e-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="3c75e-116">이 명령은 DefaultPolicy 라는 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="3c75e-117">변수</span><span class="sxs-lookup"><span data-stu-id="3c75e-117">PARAMETERS</span></span>

### <span data-ttu-id="3c75e-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3c75e-118">-BackupManagementType</span></span>
<span data-ttu-id="3c75e-119">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="3c75e-120">현재는 Add-azurevm, AzureStorage만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c75e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c75e-121">-DefaultProfile</span></span>
<span data-ttu-id="3c75e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c75e-123">-이름</span><span class="sxs-lookup"><span data-stu-id="3c75e-123">-Name</span></span>
<span data-ttu-id="3c75e-124">정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c75e-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3c75e-125">-VaultId</span></span>
<span data-ttu-id="3c75e-126">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c75e-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="3c75e-127">-WorkloadType</span></span>
<span data-ttu-id="3c75e-128">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-128">Specifies the workload type.</span></span>
<span data-ttu-id="3c75e-129">현재는 Add-azurevm, AzureFiles 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c75e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c75e-130">CommonParameters</span></span>
<span data-ttu-id="3c75e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c75e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c75e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c75e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c75e-133">입력</span><span class="sxs-lookup"><span data-stu-id="3c75e-133">INPUTS</span></span>

### <span data-ttu-id="3c75e-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c75e-134">System.String</span></span>

## <span data-ttu-id="3c75e-135">출력</span><span class="sxs-lookup"><span data-stu-id="3c75e-135">OUTPUTS</span></span>

### <span data-ttu-id="3c75e-136">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="3c75e-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="3c75e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="3c75e-137">NOTES</span></span>

## <span data-ttu-id="3c75e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c75e-138">RELATED LINKS</span></span>

[<span data-ttu-id="3c75e-139">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c75e-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3c75e-140">제거-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c75e-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3c75e-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c75e-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

