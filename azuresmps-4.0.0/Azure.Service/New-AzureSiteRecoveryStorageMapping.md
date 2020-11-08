---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045975"
---
# <span data-ttu-id="4124c-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="4124c-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="4124c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4124c-102">SYNOPSIS</span></span>
<span data-ttu-id="4124c-103">Azure 저장소 개체와 복구 저장소 개체 간의 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="4124c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4124c-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4124c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4124c-105">DESCRIPTION</span></span>
<span data-ttu-id="4124c-106">**AzureSiteRecoveryStorageMapping** Cmdlet은 Azure Site Recovery 관리 기본 Azure 저장소 개체와 복구 저장소 개체 간의 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="4124c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4124c-107">EXAMPLES</span></span>

### <span data-ttu-id="4124c-108">예제 1: 저장소 개체와 복구 저장소 개체 간의 매핑 만들기</span><span class="sxs-lookup"><span data-stu-id="4124c-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="4124c-109">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="4124c-110">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="4124c-111">두 번째 명령은 $Servers 배열의 첫 번째 서버에 대 한 사이트 복구 저장소를 가져온 다음 $Storages에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="4124c-112">마지막 명령은 기본 네트워크와 복구 네트워크 간에 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="4124c-113">이 명령은 $Storages의 첫 번째 요소로 기본 저장소 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="4124c-114">명령은 $Storages의 두 번째 요소로 복구 저장소 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="4124c-115">변수</span><span class="sxs-lookup"><span data-stu-id="4124c-115">PARAMETERS</span></span>

### <span data-ttu-id="4124c-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="4124c-116">-PrimaryStorage</span></span>
<span data-ttu-id="4124c-117">복구 저장소에 매핑할 기본 저장소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="4124c-118">**Asrstorage** 개체를 얻으려면 Get-AzureSiteRecoveryStorage cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4124c-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="4124c-119">-Profile</span></span>
<span data-ttu-id="4124c-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4124c-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4124c-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="4124c-122">-RecoveryStorage</span></span>
<span data-ttu-id="4124c-123">복구 저장소 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="4124c-124">이 cmdlet은이 매개 변수에서 지정 하는 저장소 개체에 기본 저장소 개체를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="4124c-125">**Asrstorage** 개체를 얻으려면 **get-help를 AzureSiteRecoveryStorage** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4124c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4124c-126">CommonParameters</span></span>
<span data-ttu-id="4124c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4124c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4124c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4124c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4124c-129">입력</span><span class="sxs-lookup"><span data-stu-id="4124c-129">INPUTS</span></span>

## <span data-ttu-id="4124c-130">출력</span><span class="sxs-lookup"><span data-stu-id="4124c-130">OUTPUTS</span></span>

## <span data-ttu-id="4124c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4124c-131">NOTES</span></span>

## <span data-ttu-id="4124c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4124c-132">RELATED LINKS</span></span>

[<span data-ttu-id="4124c-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="4124c-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="4124c-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="4124c-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="4124c-135">제거-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="4124c-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


