---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046110"
---
# <span data-ttu-id="9cf61-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9cf61-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="9cf61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cf61-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf61-103">사이트 복구 자격 증명 모음에서 네트워크 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="9cf61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cf61-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf61-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9cf61-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf61-106">**AzureSiteRecoveryNetworkMapping** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에서 네트워크 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9cf61-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9cf61-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf61-108">예제 1: 네트워크와 복구 네트워크 간의 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="9cf61-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="9cf61-109">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="9cf61-110">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9cf61-111">두 번째 명령은 기본 네트워크와 복구 네트워크 간의 매핑을 가져온 다음 $NetworkMapping 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="9cf61-112">명령이 네트워크 매핑의 기본 서버를 $Servers의 첫 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="9cf61-113">명령은 복구 네트워크에 대 한 서버를 $Servers의 두 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="9cf61-114">마지막 명령은 $NetworkMapping에서 네트워크 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="9cf61-115">예제 2: 네트워크와 Azure 가상 컴퓨터 네트워크 간의 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="9cf61-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="9cf61-116">첫 번째 명령 cmdlet은 현재 사이트 복구 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="9cf61-117">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9cf61-118">두 번째 명령은 기본 네트워크와 Azure 가상 컴퓨터 네트워크 간의 매핑을 가져온 다음 $NetworkMapping 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="9cf61-119">명령은 $Servers의 첫 번째 요소로 네트워크의 기본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="9cf61-120">명령은 *Azure* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="9cf61-121">따라서 명령은 Azure virtual machine 네트워크에 대 한 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="9cf61-122">마지막 명령은 $NetworkMapping에서 네트워크 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="9cf61-123">변수</span><span class="sxs-lookup"><span data-stu-id="9cf61-123">PARAMETERS</span></span>

### <span data-ttu-id="9cf61-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9cf61-124">-NetworkMapping</span></span>
<span data-ttu-id="9cf61-125">제거할 네트워크 매핑을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf61-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="9cf61-126">-Profile</span></span>
<span data-ttu-id="9cf61-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cf61-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9cf61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf61-129">CommonParameters</span></span>
<span data-ttu-id="9cf61-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf61-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf61-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf61-132">입력</span><span class="sxs-lookup"><span data-stu-id="9cf61-132">INPUTS</span></span>

## <span data-ttu-id="9cf61-133">출력</span><span class="sxs-lookup"><span data-stu-id="9cf61-133">OUTPUTS</span></span>

## <span data-ttu-id="9cf61-134">상속자</span><span class="sxs-lookup"><span data-stu-id="9cf61-134">NOTES</span></span>

## <span data-ttu-id="9cf61-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cf61-135">RELATED LINKS</span></span>

[<span data-ttu-id="9cf61-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9cf61-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="9cf61-137">새로운 AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9cf61-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="9cf61-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9cf61-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


