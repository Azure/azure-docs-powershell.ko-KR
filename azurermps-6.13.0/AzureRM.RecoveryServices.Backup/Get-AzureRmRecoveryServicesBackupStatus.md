---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703815"
---
# <span data-ttu-id="c2310-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="c2310-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="c2310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2310-102">SYNOPSIS</span></span>
<span data-ttu-id="c2310-103">ARM 리소스가 백업 되었는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2310-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2310-104">SYNTAX</span></span>

### <span data-ttu-id="c2310-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2310-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2310-106">I</span><span class="sxs-lookup"><span data-stu-id="c2310-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2310-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c2310-107">DESCRIPTION</span></span>
<span data-ttu-id="c2310-108">지정 된 리소스가 구독의 복구 서비스 자격 증명 모음에서 보호 되지 않으면 명령이 null을 반환 하거나 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="c2310-109">보호 된 경우 관련 자격 증명 모음 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="c2310-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2310-110">EXAMPLES</span></span>

### <span data-ttu-id="c2310-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2310-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="c2310-112">변수</span><span class="sxs-lookup"><span data-stu-id="c2310-112">PARAMETERS</span></span>

### <span data-ttu-id="c2310-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2310-113">-DefaultProfile</span></span>
<span data-ttu-id="c2310-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2310-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c2310-115">-Name</span></span>
<span data-ttu-id="c2310-116">구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="c2310-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2310-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2310-118">구독에서 일부 RecoveryServices 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="c2310-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2310-119">-ResourceId</span></span>
<span data-ttu-id="c2310-120">구독에서 일부 RecoveryServices 자격 증명 모음이 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2310-121">-Type</span><span class="sxs-lookup"><span data-stu-id="c2310-121">-Type</span></span>
<span data-ttu-id="c2310-122">구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2310-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2310-123">CommonParameters</span></span>
<span data-ttu-id="c2310-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2310-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2310-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2310-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2310-126">입력</span><span class="sxs-lookup"><span data-stu-id="c2310-126">INPUTS</span></span>

### <span data-ttu-id="c2310-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2310-127">System.String</span></span>

## <span data-ttu-id="c2310-128">출력</span><span class="sxs-lookup"><span data-stu-id="c2310-128">OUTPUTS</span></span>

### <span data-ttu-id="c2310-129">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="c2310-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="c2310-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c2310-130">NOTES</span></span>

## <span data-ttu-id="c2310-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2310-131">RELATED LINKS</span></span>
