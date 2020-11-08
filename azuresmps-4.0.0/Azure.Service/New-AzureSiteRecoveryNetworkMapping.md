---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046217"
---
# <span data-ttu-id="5a49c-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5a49c-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="5a49c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a49c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a49c-103">가상 네트워크 간에 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="5a49c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a49c-104">SYNTAX</span></span>

### <span data-ttu-id="5a49c-105">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="5a49c-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a49c-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5a49c-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a49c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5a49c-107">DESCRIPTION</span></span>
<span data-ttu-id="5a49c-108">**AzureSiteRecoveryNetworkMapping** cmdlet은 두 가상 네트워크 간의 매핑을 만들고 Azure Site Recovery 작업을 추적 하기 위해 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="5a49c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5a49c-109">EXAMPLES</span></span>

### <span data-ttu-id="5a49c-110">예제 1: 네트워크와 복구 네트워크 간의 매핑 만들기</span><span class="sxs-lookup"><span data-stu-id="5a49c-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="5a49c-111">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="5a49c-112">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="5a49c-113">두 번째 명령은 **AzureSiteRecoveryNetwork** cmdlet을 사용 하 여 $Servers 배열의 첫 번째 서버에 대 한 사이트 복구 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="5a49c-114">명령이 네트워크를 $Networks 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="5a49c-115">마지막 명령은 기본 네트워크와 복구 네트워크 간에 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="5a49c-116">명령은 $Networks의 첫 번째 요소로 기본 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="5a49c-117">명령은 $Networks의 두 번째 요소로 복구 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="5a49c-118">변수</span><span class="sxs-lookup"><span data-stu-id="5a49c-118">PARAMETERS</span></span>

### <span data-ttu-id="5a49c-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a49c-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="5a49c-120">Azure 구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a49c-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="5a49c-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="5a49c-122">Azure 가상 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a49c-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="5a49c-123">-PrimaryNetwork</span></span>
<span data-ttu-id="5a49c-124">주 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a49c-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="5a49c-125">-Profile</span></span>
<span data-ttu-id="5a49c-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a49c-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a49c-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="5a49c-128">-RecoveryNetwork</span></span>
<span data-ttu-id="5a49c-129">복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a49c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a49c-130">CommonParameters</span></span>
<span data-ttu-id="5a49c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a49c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a49c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a49c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a49c-133">입력</span><span class="sxs-lookup"><span data-stu-id="5a49c-133">INPUTS</span></span>

## <span data-ttu-id="5a49c-134">출력</span><span class="sxs-lookup"><span data-stu-id="5a49c-134">OUTPUTS</span></span>

## <span data-ttu-id="5a49c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5a49c-135">NOTES</span></span>

## <span data-ttu-id="5a49c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a49c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5a49c-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5a49c-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="5a49c-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="5a49c-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="5a49c-139">제거-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5a49c-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


