---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534600"
---
# <span data-ttu-id="93d8f-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93d8f-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="93d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="93d8f-103">보호 되는 항목을 만들어 보호할 수 있는 항목에 대 한 복제를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93d8f-104">SYNTAX</span></span>

### <span data-ttu-id="93d8f-105">DisableDR (기본값)</span><span class="sxs-lookup"><span data-stu-id="93d8f-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93d8f-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="93d8f-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93d8f-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="93d8f-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93d8f-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="93d8f-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d8f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="93d8f-109">DESCRIPTION</span></span>
<span data-ttu-id="93d8f-110">**AzureRmSiteRecoveryReplicationProtectedItem** cmdlet은 새 복제 보호 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="93d8f-111">보호 가능한 항목에 대 한 복제를 사용 하도록 설정 하려면이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="93d8f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="93d8f-112">EXAMPLES</span></span>

## <span data-ttu-id="93d8f-113">변수</span><span class="sxs-lookup"><span data-stu-id="93d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="93d8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d8f-114">-DefaultProfile</span></span>
<span data-ttu-id="93d8f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d8f-116">-이름</span><span class="sxs-lookup"><span data-stu-id="93d8f-116">-Name</span></span>
<span data-ttu-id="93d8f-117">Azure Site Recovery 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-118">-OS</span><span class="sxs-lookup"><span data-stu-id="93d8f-118">-OS</span></span>
<span data-ttu-id="93d8f-119">운영 체제 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-119">Specifies the operating system family.</span></span>
<span data-ttu-id="93d8f-120">이 매개 변수에 허용 되는 값은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="93d8f-121">-OSDiskName</span></span>
<span data-ttu-id="93d8f-122">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="93d8f-123">-ProtectableItem</span></span>
<span data-ttu-id="93d8f-124">Azure Site Recovery 보호 가능한 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="93d8f-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="93d8f-126">복제에 사용할 Azure Site Recovery 보호 컨테이너 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="93d8f-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="93d8f-128">이 cmdlet이 복제 하는 Azure 저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="93d8f-129">-WaitForCompletion</span></span>
<span data-ttu-id="93d8f-130">Cmdlet이 완료 될 때까지 대기 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-130">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="93d8f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="93d8f-131">-Confirm</span></span>
<span data-ttu-id="93d8f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d8f-133">-WhatIf</span></span>
<span data-ttu-id="93d8f-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="93d8f-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d8f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d8f-136">CommonParameters</span></span>
<span data-ttu-id="93d8f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d8f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d8f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d8f-139">입력</span><span class="sxs-lookup"><span data-stu-id="93d8f-139">INPUTS</span></span>

### <span data-ttu-id="93d8f-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="93d8f-140">ASRProtectableItem</span></span>
<span data-ttu-id="93d8f-141">' ProtectableItem ' 매개 변수는 파이프라인에서 ' ASRProtectableItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d8f-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="93d8f-142">출력</span><span class="sxs-lookup"><span data-stu-id="93d8f-142">OUTPUTS</span></span>

### <span data-ttu-id="93d8f-143">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="93d8f-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="93d8f-144">상속자</span><span class="sxs-lookup"><span data-stu-id="93d8f-144">NOTES</span></span>

## <span data-ttu-id="93d8f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93d8f-145">RELATED LINKS</span></span>

[<span data-ttu-id="93d8f-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93d8f-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="93d8f-147">제거-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93d8f-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="93d8f-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93d8f-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
