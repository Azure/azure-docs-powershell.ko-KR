---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044719"
---
# <span data-ttu-id="aed14-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="aed14-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="aed14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed14-102">SYNOPSIS</span></span>
<span data-ttu-id="aed14-103">ARM 리소스가 백업 되었는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="aed14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aed14-104">SYNTAX</span></span>

### <span data-ttu-id="aed14-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="aed14-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed14-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="aed14-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed14-107">I</span><span class="sxs-lookup"><span data-stu-id="aed14-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aed14-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aed14-108">DESCRIPTION</span></span>
<span data-ttu-id="aed14-109">지정 된 리소스가 구독의 복구 서비스 자격 증명 모음에서 보호 되지 않으면 명령이 null을 반환 하거나 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="aed14-110">보호 된 경우 관련 자격 증명 모음 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="aed14-111">예제의</span><span class="sxs-lookup"><span data-stu-id="aed14-111">EXAMPLES</span></span>

### <span data-ttu-id="aed14-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="aed14-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="aed14-113">변수</span><span class="sxs-lookup"><span data-stu-id="aed14-113">PARAMETERS</span></span>

### <span data-ttu-id="aed14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed14-114">-DefaultProfile</span></span>
<span data-ttu-id="aed14-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aed14-116">-이름</span><span class="sxs-lookup"><span data-stu-id="aed14-116">-Name</span></span>
<span data-ttu-id="aed14-117">구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed14-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="aed14-118">-ProtectableObjectName</span></span>
<span data-ttu-id="aed14-119">구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed14-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed14-120">-ResourceGroupName</span></span>
<span data-ttu-id="aed14-121">구독에서 일부 RecoveryServices 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed14-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aed14-122">-ResourceId</span></span>
<span data-ttu-id="aed14-123">구독에서 일부 RecoveryServices 자격 증명 모음이 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed14-124">-Type</span><span class="sxs-lookup"><span data-stu-id="aed14-124">-Type</span></span>
<span data-ttu-id="aed14-125">구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed14-126">CommonParameters</span></span>
<span data-ttu-id="aed14-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed14-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aed14-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed14-129">입력</span><span class="sxs-lookup"><span data-stu-id="aed14-129">INPUTS</span></span>

### <span data-ttu-id="aed14-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aed14-130">System.String</span></span>

## <span data-ttu-id="aed14-131">출력</span><span class="sxs-lookup"><span data-stu-id="aed14-131">OUTPUTS</span></span>

### <span data-ttu-id="aed14-132">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="aed14-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="aed14-133">상속자</span><span class="sxs-lookup"><span data-stu-id="aed14-133">NOTES</span></span>

## <span data-ttu-id="aed14-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aed14-134">RELATED LINKS</span></span>
