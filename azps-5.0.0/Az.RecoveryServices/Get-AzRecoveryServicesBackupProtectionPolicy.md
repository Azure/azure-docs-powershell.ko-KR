---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308972"
---
# <span data-ttu-id="e198b-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e198b-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="e198b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e198b-102">SYNOPSIS</span></span>
<span data-ttu-id="e198b-103">자격 증명 모음에 대 한 백업 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="e198b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e198b-104">SYNTAX</span></span>

### <span data-ttu-id="e198b-105">NoParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e198b-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e198b-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="e198b-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e198b-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="e198b-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e198b-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="e198b-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e198b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e198b-109">DESCRIPTION</span></span>
<span data-ttu-id="e198b-110">**AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 대 한 Azure Backup 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="e198b-111">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e198b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e198b-112">EXAMPLES</span></span>

### <span data-ttu-id="e198b-113">예제 1: 자격 증명 모음에서 모든 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e198b-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="e198b-114">이 명령은 자격 증명 모음에서 만들어진 모든 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="e198b-115">예제 2: 특정 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e198b-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="e198b-116">이 명령은 DefaultPolicy 라는 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="e198b-117">변수</span><span class="sxs-lookup"><span data-stu-id="e198b-117">PARAMETERS</span></span>

### <span data-ttu-id="e198b-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e198b-118">-BackupManagementType</span></span>
<span data-ttu-id="e198b-119">보호 되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-119">The class of resources being protected.</span></span> <span data-ttu-id="e198b-120">현재이 cmdlet에 대해 지원 되는 값은 Add-azurevm, AzureStorage, Azurestorage입니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

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

### <span data-ttu-id="e198b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e198b-121">-DefaultProfile</span></span>
<span data-ttu-id="e198b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e198b-123">-이름</span><span class="sxs-lookup"><span data-stu-id="e198b-123">-Name</span></span>
<span data-ttu-id="e198b-124">정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="e198b-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e198b-125">-VaultId</span></span>
<span data-ttu-id="e198b-126">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e198b-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e198b-127">-WorkloadType</span></span>
<span data-ttu-id="e198b-128">리소스의 작업 부하 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-128">Workload type of the resource.</span></span> <span data-ttu-id="e198b-129">현재 지원 되는 값은 Add-azurevm, AzureFiles, MSSQL입니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="e198b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e198b-130">CommonParameters</span></span>
<span data-ttu-id="e198b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e198b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e198b-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e198b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e198b-133">입력</span><span class="sxs-lookup"><span data-stu-id="e198b-133">INPUTS</span></span>

### <span data-ttu-id="e198b-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e198b-134">System.String</span></span>

## <span data-ttu-id="e198b-135">출력</span><span class="sxs-lookup"><span data-stu-id="e198b-135">OUTPUTS</span></span>

### <span data-ttu-id="e198b-136">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="e198b-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="e198b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e198b-137">NOTES</span></span>

## <span data-ttu-id="e198b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e198b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e198b-139">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e198b-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e198b-140">제거-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e198b-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e198b-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e198b-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


