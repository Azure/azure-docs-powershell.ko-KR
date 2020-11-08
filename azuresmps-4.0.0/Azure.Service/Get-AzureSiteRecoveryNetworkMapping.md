---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045590"
---
# <span data-ttu-id="a3a8c-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a3a8c-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="a3a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a8c-103">사이트 복구 자격 증명 모음에 대 한 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="a3a8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3a8c-104">SYNTAX</span></span>

### <span data-ttu-id="a3a8c-105">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="a3a8c-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a3a8c-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="a3a8c-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a8c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a3a8c-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a8c-108">**AzureSiteRecoveryNetworkMapping** cmdlet은 현재 사이트 복구 자격 증명 모음에 대 한 Azure Site recovery 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="a3a8c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a3a8c-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a8c-110">예제 1: 네트워크와 복구 네트워크 간의 매핑 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3a8c-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="a3a8c-111">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="a3a8c-112">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="a3a8c-113">두 번째 명령은 기본 네트워크와 복구 네트워크 간의 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="a3a8c-114">명령이 네트워크 매핑의 기본 서버를 $Servers의 첫 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="a3a8c-115">명령은 복구 네트워크에 대 한 서버를 $Servers의 두 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="a3a8c-116">예제 2: 네트워크와 Azure 가상 컴퓨터 네트워크 간의 매핑 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3a8c-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="a3a8c-117">첫 번째 명령 cmdlet은 현재 사이트 복구 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="a3a8c-118">명령이 $Servers 배열 변수에 서버를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="a3a8c-119">두 번째 명령은 기본 네트워크와 Azure 가상 컴퓨터 네트워크 간의 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="a3a8c-120">명령은 $Servers의 첫 번째 요소로 네트워크의 기본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="a3a8c-121">명령은 *Azure* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="a3a8c-122">따라서 명령은 Azure virtual machine 네트워크에 대 한 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="a3a8c-123">변수</span><span class="sxs-lookup"><span data-stu-id="a3a8c-123">PARAMETERS</span></span>

### <span data-ttu-id="a3a8c-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="a3a8c-124">-Azure</span></span>
<span data-ttu-id="a3a8c-125">이 cmdlet이 Azure 가상 네트워크에 매핑된 주 서버에서 네트워크에 대 한 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a8c-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="a3a8c-126">-PrimaryServer</span></span>
<span data-ttu-id="a3a8c-127">매핑을 가져올 주 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a8c-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="a3a8c-128">-Profile</span></span>
<span data-ttu-id="a3a8c-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3a8c-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3a8c-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="a3a8c-131">-RecoveryServer</span></span>
<span data-ttu-id="a3a8c-132">매핑을 가져올 복구 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a8c-133">CommonParameters</span></span>
<span data-ttu-id="a3a8c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a8c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a8c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a8c-136">입력</span><span class="sxs-lookup"><span data-stu-id="a3a8c-136">INPUTS</span></span>

## <span data-ttu-id="a3a8c-137">출력</span><span class="sxs-lookup"><span data-stu-id="a3a8c-137">OUTPUTS</span></span>

## <span data-ttu-id="a3a8c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a3a8c-138">NOTES</span></span>

## <span data-ttu-id="a3a8c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3a8c-139">RELATED LINKS</span></span>

[<span data-ttu-id="a3a8c-140">새로운 AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a3a8c-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="a3a8c-141">제거-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a3a8c-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


