---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046109"
---
# <span data-ttu-id="b82e3-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b82e3-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="b82e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b82e3-103">사이트 복구 자격 증명 모음에 대 한 저장소 개체 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="b82e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b82e3-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b82e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b82e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b82e3-106">**AzureSiteRecoveryStorageMapping** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대 한 저장소 개체 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b82e3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b82e3-107">EXAMPLES</span></span>

### <span data-ttu-id="b82e3-108">예제 1: 네트워크와 복구 네트워크 간의 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="b82e3-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="b82e3-109">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b82e3-110">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b82e3-111">두 번째 명령은 두 저장소 개체 간의 매핑을 가져온 다음 $StorageMapping 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="b82e3-112">명령이 네트워크 매핑의 기본 서버를 $Servers의 첫 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="b82e3-113">명령은 복구 네트워크에 대 한 서버를 $Servers의 두 번째 요소로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="b82e3-114">마지막 명령은 $StorageMapping에서 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="b82e3-115">변수</span><span class="sxs-lookup"><span data-stu-id="b82e3-115">PARAMETERS</span></span>

### <span data-ttu-id="b82e3-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="b82e3-116">-Profile</span></span>
<span data-ttu-id="b82e3-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b82e3-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b82e3-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="b82e3-119">-StorageMapping</span></span>
<span data-ttu-id="b82e3-120">네트워크 매핑을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-120">Specifies a network mapping.</span></span>
<span data-ttu-id="b82e3-121">**ASRStorageMapping** 을 얻으려면 **AzureSiteRecoveryStorage** cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82e3-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b82e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82e3-122">CommonParameters</span></span>
<span data-ttu-id="b82e3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82e3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b82e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82e3-125">입력</span><span class="sxs-lookup"><span data-stu-id="b82e3-125">INPUTS</span></span>

## <span data-ttu-id="b82e3-126">출력</span><span class="sxs-lookup"><span data-stu-id="b82e3-126">OUTPUTS</span></span>

## <span data-ttu-id="b82e3-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b82e3-127">NOTES</span></span>

## <span data-ttu-id="b82e3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b82e3-128">RELATED LINKS</span></span>

[<span data-ttu-id="b82e3-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="b82e3-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


