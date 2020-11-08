---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045575"
---
# <span data-ttu-id="d818f-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="d818f-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="d818f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d818f-102">SYNOPSIS</span></span>
<span data-ttu-id="d818f-103">자격 증명 모음에 대 한 사이트 복구 저장소 개체의 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="d818f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d818f-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d818f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d818f-105">DESCRIPTION</span></span>
<span data-ttu-id="d818f-106">**AzureSiteRecoveryStorageMapping** cmdlet은 현재 Azure site recovery 자격 증명 모음에 대 한 Azure Site recovery 저장소 개체의 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d818f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d818f-107">EXAMPLES</span></span>

### <span data-ttu-id="d818f-108">예제 1: 저장소 개체와 복구 저장소 개체 간의 매핑 가져오기</span><span class="sxs-lookup"><span data-stu-id="d818f-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="d818f-109">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="d818f-110">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="d818f-111">두 번째 명령은 두 Azure 저장소 개체 간의 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="d818f-112">이 명령은 $Servers의 첫 번째 요소로 저장소 개체 매핑에 대 한 기본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="d818f-113">명령은 복구 저장소 개체에 대 한 서버를 $Servers의 두 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="d818f-114">변수</span><span class="sxs-lookup"><span data-stu-id="d818f-114">PARAMETERS</span></span>

### <span data-ttu-id="d818f-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="d818f-115">-PrimaryServer</span></span>
<span data-ttu-id="d818f-116">주 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-116">Specifies the primary server.</span></span>
<span data-ttu-id="d818f-117">서버를 얻으려면 **Get-AzureSiteRecoveryServer** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

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

### <span data-ttu-id="d818f-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="d818f-118">-Profile</span></span>
<span data-ttu-id="d818f-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d818f-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d818f-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d818f-121">-RecoveryServer</span></span>
<span data-ttu-id="d818f-122">복구 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-122">Specifies the recovery server.</span></span>
<span data-ttu-id="d818f-123">서버를 얻으려면 **get-help를 AzureSiteRecoveryServer** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

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

### <span data-ttu-id="d818f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d818f-124">CommonParameters</span></span>
<span data-ttu-id="d818f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d818f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d818f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d818f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d818f-127">입력</span><span class="sxs-lookup"><span data-stu-id="d818f-127">INPUTS</span></span>

## <span data-ttu-id="d818f-128">출력</span><span class="sxs-lookup"><span data-stu-id="d818f-128">OUTPUTS</span></span>

## <span data-ttu-id="d818f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d818f-129">NOTES</span></span>

## <span data-ttu-id="d818f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d818f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d818f-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d818f-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="d818f-132">새로운 AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="d818f-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="d818f-133">제거-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="d818f-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


