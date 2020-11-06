---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 7cfc764e5c9c3c5bb11290220cc04b2baa781070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532908"
---
# <span data-ttu-id="be361-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="be361-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="be361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be361-102">SYNOPSIS</span></span>
<span data-ttu-id="be361-103">사이트 복구 보호 엔터티의 복구 쪽 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be361-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be361-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be361-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be361-105">DESCRIPTION</span></span>
<span data-ttu-id="be361-106">**AzureRmSiteRecoveryVM** cmdlet은 복구 가상 컴퓨터 크기 및 복구 가상 컴퓨터 네트워크와 같은 Azure Site recovery 보호 엔터티의 복구 쪽 보호 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="be361-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be361-107">EXAMPLES</span></span>

## <span data-ttu-id="be361-108">변수</span><span class="sxs-lookup"><span data-stu-id="be361-108">PARAMETERS</span></span>

### <span data-ttu-id="be361-109">-이름</span><span class="sxs-lookup"><span data-stu-id="be361-109">-Name</span></span>
<span data-ttu-id="be361-110">대상 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-110">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="be361-111">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="be361-111">-NicSelectionType</span></span>
<span data-ttu-id="be361-112">네트워크 어댑터 선택 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-112">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="be361-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be361-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be361-114">NotSelected</span><span class="sxs-lookup"><span data-stu-id="be361-114">NotSelected</span></span>
- <span data-ttu-id="be361-115">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="be361-115">SelectedByUser</span></span>

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

### <span data-ttu-id="be361-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="be361-116">-PrimaryNic</span></span>
<span data-ttu-id="be361-117">주 네트워크 어댑터 카드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-117">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="be361-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="be361-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="be361-119">복구 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-119">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="be361-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="be361-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="be361-121">복구 시 주 네트워크 어댑터 컨트롤러에 할당 되는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-121">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="be361-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="be361-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="be361-123">복구 시 주 네트워크 어댑터 컨트롤러를 연결 하는 데 사용할 Azure 가상 네트워크 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-123">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="be361-124">-크기</span><span class="sxs-lookup"><span data-stu-id="be361-124">-Size</span></span>
<span data-ttu-id="be361-125">대상 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-125">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="be361-126">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="be361-126">-VirtualMachine</span></span>
<span data-ttu-id="be361-127">사이트 복구 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-127">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be361-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be361-128">-DefaultProfile</span></span>
<span data-ttu-id="be361-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be361-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be361-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be361-130">CommonParameters</span></span>
<span data-ttu-id="be361-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be361-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be361-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be361-133">입력</span><span class="sxs-lookup"><span data-stu-id="be361-133">INPUTS</span></span>

### <span data-ttu-id="be361-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="be361-134">ASRVirtualMachine</span></span>
<span data-ttu-id="be361-135">' VirtualMachine ' 매개 변수는 파이프라인에서 ' ASRVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be361-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="be361-136">출력</span><span class="sxs-lookup"><span data-stu-id="be361-136">OUTPUTS</span></span>

### <span data-ttu-id="be361-137">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="be361-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="be361-138">상속자</span><span class="sxs-lookup"><span data-stu-id="be361-138">NOTES</span></span>

## <span data-ttu-id="be361-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be361-139">RELATED LINKS</span></span>

[<span data-ttu-id="be361-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="be361-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
