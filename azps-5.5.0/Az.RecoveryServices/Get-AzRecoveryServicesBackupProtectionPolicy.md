---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202025"
---
# <span data-ttu-id="16dfe-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="16dfe-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="16dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="16dfe-103">자격 증명 모음에 대한 Backup 보호 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="16dfe-104">구문</span><span class="sxs-lookup"><span data-stu-id="16dfe-104">SYNTAX</span></span>

### <span data-ttu-id="16dfe-105">NoParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="16dfe-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16dfe-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="16dfe-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16dfe-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="16dfe-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16dfe-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="16dfe-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16dfe-109">설명</span><span class="sxs-lookup"><span data-stu-id="16dfe-109">DESCRIPTION</span></span>
<span data-ttu-id="16dfe-110">**Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대한 Azure Backup 보호 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="16dfe-111">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="16dfe-112">예제</span><span class="sxs-lookup"><span data-stu-id="16dfe-112">EXAMPLES</span></span>

### <span data-ttu-id="16dfe-113">예제 1: 자격 증명 모음의 모든 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="16dfe-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="16dfe-114">이 명령은 자격 증명 모음에서 만든 모든 보호 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="16dfe-115">예제 2: 특정 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="16dfe-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="16dfe-116">이 명령은 DefaultPolicy라는 보호 정책을 엽서로 $Pol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="16dfe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16dfe-117">PARAMETERS</span></span>

### <span data-ttu-id="16dfe-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="16dfe-118">-BackupManagementType</span></span>
<span data-ttu-id="16dfe-119">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-119">The class of resources being protected.</span></span> <span data-ttu-id="16dfe-120">현재 이 cmdlet에 지원되는 값은 AzureVM, AzureStorage, AzureWorkload입니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dfe-121">-DefaultProfile</span></span>
<span data-ttu-id="16dfe-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16dfe-123">-Name</span><span class="sxs-lookup"><span data-stu-id="16dfe-123">-Name</span></span>
<span data-ttu-id="16dfe-124">정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="16dfe-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="16dfe-125">-VaultId</span></span>
<span data-ttu-id="16dfe-126">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="16dfe-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="16dfe-127">-WorkloadType</span></span>
<span data-ttu-id="16dfe-128">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-128">Workload type of the resource.</span></span> <span data-ttu-id="16dfe-129">현재 지원되는 값은 AzureVM, AzureFiles, MSSQL입니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="16dfe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dfe-130">CommonParameters</span></span>
<span data-ttu-id="16dfe-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16dfe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dfe-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16dfe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dfe-133">입력</span><span class="sxs-lookup"><span data-stu-id="16dfe-133">INPUTS</span></span>

### <span data-ttu-id="16dfe-134">System.String</span><span class="sxs-lookup"><span data-stu-id="16dfe-134">System.String</span></span>

## <span data-ttu-id="16dfe-135">출력</span><span class="sxs-lookup"><span data-stu-id="16dfe-135">OUTPUTS</span></span>

### <span data-ttu-id="16dfe-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="16dfe-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="16dfe-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16dfe-137">NOTES</span></span>

## <span data-ttu-id="16dfe-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16dfe-138">RELATED LINKS</span></span>

[<span data-ttu-id="16dfe-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="16dfe-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="16dfe-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="16dfe-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="16dfe-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="16dfe-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


