---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529109"
---
# <span data-ttu-id="77845-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77845-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="77845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77845-102">SYNOPSIS</span></span>
<span data-ttu-id="77845-103">복제 보호 항목에 대 한 대상 네트워크 및 가상 컴퓨터 크기와 같은 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77845-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77845-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77845-105">설명은</span><span class="sxs-lookup"><span data-stu-id="77845-105">DESCRIPTION</span></span>
<span data-ttu-id="77845-106">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet은 복제 보호 항목에 대 한 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="77845-107">예제의</span><span class="sxs-lookup"><span data-stu-id="77845-107">EXAMPLES</span></span>

## <span data-ttu-id="77845-108">변수</span><span class="sxs-lookup"><span data-stu-id="77845-108">PARAMETERS</span></span>

### <span data-ttu-id="77845-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="77845-109">-LicenseType</span></span>
<span data-ttu-id="77845-110">하이브리드 사용 혜택을 통해 마이그레이션된 Windows Server 가상 컴퓨터에 대 한 라이선스 종류 선택을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-111">-이름</span><span class="sxs-lookup"><span data-stu-id="77845-111">-Name</span></span>
<span data-ttu-id="77845-112">복구 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-112">Specifies the name of the recovery virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="77845-113">-NicSelectionType</span></span>
<span data-ttu-id="77845-114">사용자가 설정 하거나 기본적으로 설정 되는 NIC (네트워크 인터페이스 카드) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="77845-115">NotSelected를 지정 하 여 기본 값으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77845-115">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="77845-116">-PrimaryNic</span></span>
<span data-ttu-id="77845-117">이 cmdlet이 복구 네트워크 속성을 설정 하는 가상 컴퓨터의 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="77845-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="77845-119">이 cmdlet이 보호 된 항목을 복구 하는 Azure 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="77845-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="77845-121">복구 시 기본 NIC에 할당 해야 하는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="77845-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="77845-123">이 cmdlet이 보호 된 항목을 복구 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77845-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="77845-125">Azure Site Recovery 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77845-126">-크기</span><span class="sxs-lookup"><span data-stu-id="77845-126">-Size</span></span>
<span data-ttu-id="77845-127">복구 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="77845-128">값은 Azure 가상 머신에서 지원 되는 크기 집합에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77845-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77845-129">-DefaultProfile</span></span>
<span data-ttu-id="77845-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77845-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77845-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77845-131">CommonParameters</span></span>
<span data-ttu-id="77845-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77845-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77845-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77845-134">입력</span><span class="sxs-lookup"><span data-stu-id="77845-134">INPUTS</span></span>

### <span data-ttu-id="77845-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77845-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="77845-136">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="77845-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="77845-137">출력</span><span class="sxs-lookup"><span data-stu-id="77845-137">OUTPUTS</span></span>

### <span data-ttu-id="77845-138">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="77845-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="77845-139">상속자</span><span class="sxs-lookup"><span data-stu-id="77845-139">NOTES</span></span>

## <span data-ttu-id="77845-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77845-140">RELATED LINKS</span></span>

[<span data-ttu-id="77845-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77845-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="77845-142">새로운 AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77845-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="77845-143">제거-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77845-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
