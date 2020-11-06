---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529212"
---
# <span data-ttu-id="9ee87-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9ee87-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="9ee87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee87-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee87-103">지정 된 백업 보호 정책이 있는 항목에 대해 백업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ee87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ee87-104">SYNTAX</span></span>

### <span data-ttu-id="9ee87-105">AzureVMComputeEnableProtection (기본값)</span><span class="sxs-lookup"><span data-stu-id="9ee87-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ee87-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="9ee87-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ee87-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="9ee87-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee87-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9ee87-108">DESCRIPTION</span></span>
<span data-ttu-id="9ee87-109">**AzureRmRecoveryServicesBackupProtection** cmdlet은 항목에 대 한 Azure 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="9ee87-110">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9ee87-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9ee87-111">EXAMPLES</span></span>

### <span data-ttu-id="9ee87-112">예제 1: 항목에 대해 백업 보호 사용</span><span class="sxs-lookup"><span data-stu-id="9ee87-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="9ee87-113">첫 번째 cmdlet은 기본 정책 개체를 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="9ee87-114">두 번째 cmdlet은 $Pol의 정책을 사용 하 여 V2VM 이라는 ARM 가상 컴퓨터에 대 한 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="9ee87-115">변수</span><span class="sxs-lookup"><span data-stu-id="9ee87-115">PARAMETERS</span></span>

### <span data-ttu-id="9ee87-116">-항목</span><span class="sxs-lookup"><span data-stu-id="9ee87-116">-Item</span></span>
<span data-ttu-id="9ee87-117">이 cmdlet이 보호할 수 있는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="9ee87-118">**AzureRmRecoveryServicesBackupItem** 을 얻으려면 Get-AzureRmRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee87-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9ee87-119">-Name</span></span>
<span data-ttu-id="9ee87-120">백업 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee87-121">-정책</span><span class="sxs-lookup"><span data-stu-id="9ee87-121">-Policy</span></span>
<span data-ttu-id="9ee87-122">이 cmdlet이 항목과 연결 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="9ee87-123">**AzureRmRecoveryServicesBackupProtectionPolicy** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee87-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ee87-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9ee87-126">ARM 가상 컴퓨터에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee87-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9ee87-127">-ServiceName</span></span>
<span data-ttu-id="9ee87-128">서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-128">Specifies the service name.</span></span>
<span data-ttu-id="9ee87-129">이 매개 변수는 ASM 가상 머신에만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee87-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee87-130">-DefaultProfile</span></span>
<span data-ttu-id="9ee87-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee87-132">CommonParameters</span></span>
<span data-ttu-id="9ee87-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee87-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ee87-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee87-135">입력</span><span class="sxs-lookup"><span data-stu-id="9ee87-135">INPUTS</span></span>

### <span data-ttu-id="9ee87-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="9ee87-136">ItemBase</span></span>
<span data-ttu-id="9ee87-137">' Item ' 매개 변수는 파이프라인에서 ' ItemBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee87-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="9ee87-138">출력</span><span class="sxs-lookup"><span data-stu-id="9ee87-138">OUTPUTS</span></span>

### <span data-ttu-id="9ee87-139">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="9ee87-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9ee87-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9ee87-140">NOTES</span></span>

## <span data-ttu-id="9ee87-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ee87-141">RELATED LINKS</span></span>

[<span data-ttu-id="9ee87-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9ee87-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9ee87-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9ee87-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


