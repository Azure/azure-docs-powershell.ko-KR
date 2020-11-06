---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525032"
---
# <span data-ttu-id="1666d-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="1666d-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="1666d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1666d-102">SYNOPSIS</span></span>
<span data-ttu-id="1666d-103">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1666d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1666d-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1666d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1666d-105">DESCRIPTION</span></span>
<span data-ttu-id="1666d-106">디스크를 복제 하는 데 사용 되는 캐시 저장소 계정 및 대상 저장소 계정 (복구 영역)에 Azure 가상 머신 디스크를 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="1666d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1666d-107">EXAMPLES</span></span>

### <span data-ttu-id="1666d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1666d-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="1666d-109">복제할 Azure virtual machine 디스크에 대 한 디스크 매핑 개체를 만듭니다. Azure to Azure EnableDr 및 보호 작업 중에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="1666d-110">변수</span><span class="sxs-lookup"><span data-stu-id="1666d-110">PARAMETERS</span></span>

### <span data-ttu-id="1666d-111">-확인</span><span class="sxs-lookup"><span data-stu-id="1666d-111">-Confirm</span></span>
<span data-ttu-id="1666d-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1666d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1666d-113">-DefaultProfile</span></span>
<span data-ttu-id="1666d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1666d-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1666d-115">-LogStorageAccountId</span></span>
<span data-ttu-id="1666d-116">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1666d-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1666d-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="1666d-118">복제할 Azure storage 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1666d-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="1666d-119">-VhdUri</span></span>
<span data-ttu-id="1666d-120">이 매핑이 해당 하는 디스크의 VHD URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1666d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1666d-121">-WhatIf</span></span>
<span data-ttu-id="1666d-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1666d-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1666d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1666d-124">CommonParameters</span></span>
<span data-ttu-id="1666d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1666d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1666d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1666d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1666d-127">입력</span><span class="sxs-lookup"><span data-stu-id="1666d-127">INPUTS</span></span>

### <span data-ttu-id="1666d-128">않아야</span><span class="sxs-lookup"><span data-stu-id="1666d-128">None</span></span>

## <span data-ttu-id="1666d-129">출력</span><span class="sxs-lookup"><span data-stu-id="1666d-129">OUTPUTS</span></span>

### <span data-ttu-id="1666d-130">SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="1666d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="1666d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1666d-131">NOTES</span></span>

## <span data-ttu-id="1666d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1666d-132">RELATED LINKS</span></span>
