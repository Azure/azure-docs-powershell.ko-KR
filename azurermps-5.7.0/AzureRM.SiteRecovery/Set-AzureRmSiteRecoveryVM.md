---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: b330cb59281a3f140ba30f10f31ecb5bf3b49f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534583"
---
# <span data-ttu-id="9ba58-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="9ba58-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="9ba58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba58-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba58-103">사이트 복구 보호 엔터티의 복구 쪽 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ba58-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ba58-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ba58-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba58-106">**AzureRmSiteRecoveryVM** cmdlet은 복구 가상 컴퓨터 크기 및 복구 가상 컴퓨터 네트워크와 같은 Azure Site recovery 보호 엔터티의 복구 쪽 보호 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="9ba58-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ba58-107">EXAMPLES</span></span>

## <span data-ttu-id="9ba58-108">변수</span><span class="sxs-lookup"><span data-stu-id="9ba58-108">PARAMETERS</span></span>

### <span data-ttu-id="9ba58-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba58-109">-DefaultProfile</span></span>
<span data-ttu-id="9ba58-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba58-111">-이름</span><span class="sxs-lookup"><span data-stu-id="9ba58-111">-Name</span></span>
<span data-ttu-id="9ba58-112">대상 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-112">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="9ba58-113">-NicSelectionType</span></span>
<span data-ttu-id="9ba58-114">네트워크 어댑터 선택 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-114">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="9ba58-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ba58-116">NotSelected</span><span class="sxs-lookup"><span data-stu-id="9ba58-116">NotSelected</span></span>
- <span data-ttu-id="9ba58-117">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="9ba58-117">SelectedByUser</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="9ba58-118">-PrimaryNic</span></span>
<span data-ttu-id="9ba58-119">주 네트워크 어댑터 카드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-119">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="9ba58-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="9ba58-121">복구 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="9ba58-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="9ba58-123">복구 시 주 네트워크 어댑터 컨트롤러에 할당 되는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-123">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="9ba58-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="9ba58-125">복구 시 주 네트워크 어댑터 컨트롤러를 연결 하는 데 사용할 Azure 가상 네트워크 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-125">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-126">-크기</span><span class="sxs-lookup"><span data-stu-id="9ba58-126">-Size</span></span>
<span data-ttu-id="9ba58-127">대상 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-127">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9ba58-128">-VirtualMachine</span></span>
<span data-ttu-id="9ba58-129">사이트 복구 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-129">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba58-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba58-130">CommonParameters</span></span>
<span data-ttu-id="9ba58-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba58-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba58-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba58-133">입력</span><span class="sxs-lookup"><span data-stu-id="9ba58-133">INPUTS</span></span>

### <span data-ttu-id="9ba58-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9ba58-134">ASRVirtualMachine</span></span>
<span data-ttu-id="9ba58-135">' VirtualMachine ' 매개 변수는 파이프라인에서 ' ASRVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba58-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9ba58-136">출력</span><span class="sxs-lookup"><span data-stu-id="9ba58-136">OUTPUTS</span></span>

### <span data-ttu-id="9ba58-137">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="9ba58-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9ba58-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9ba58-138">NOTES</span></span>

## <span data-ttu-id="9ba58-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba58-139">RELATED LINKS</span></span>

[<span data-ttu-id="9ba58-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="9ba58-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
