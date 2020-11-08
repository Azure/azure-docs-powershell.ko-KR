---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045593"
---
# <span data-ttu-id="7ce74-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ce74-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="7ce74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce74-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce74-103">사이트 복구 자격 증명 모음에 대 한 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="7ce74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ce74-104">SYNTAX</span></span>

### <span data-ttu-id="7ce74-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ce74-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7ce74-106">ById</span><span class="sxs-lookup"><span data-stu-id="7ce74-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7ce74-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7ce74-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7ce74-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7ce74-108">DESCRIPTION</span></span>
<span data-ttu-id="7ce74-109">**AzureSiteRecoveryProtectionContainer** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대 한 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="7ce74-110">보호 컨테이너는 가상 컴퓨터와 같은 보호 된 개체에 대 한 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="7ce74-111">보호 정책은 보호 된 항목에 대 한 복제 설정을 정의 하 고 보호 컨테이너와 연결 되어 보호 된 엔터티에 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="7ce74-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7ce74-112">EXAMPLES</span></span>

### <span data-ttu-id="7ce74-113">예제 1: 보호 된 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="7ce74-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="7ce74-114">이 명령은 현재 자격 증명 모음의 보호 된 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="7ce74-115">변수</span><span class="sxs-lookup"><span data-stu-id="7ce74-115">PARAMETERS</span></span>

### <span data-ttu-id="7ce74-116">-Id</span><span class="sxs-lookup"><span data-stu-id="7ce74-116">-Id</span></span>
<span data-ttu-id="7ce74-117">가져올 보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce74-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7ce74-118">-Name</span></span>
<span data-ttu-id="7ce74-119">가져올 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-119">Specifies the name of a protection container to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce74-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="7ce74-120">-Profile</span></span>
<span data-ttu-id="7ce74-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ce74-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ce74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce74-123">CommonParameters</span></span>
<span data-ttu-id="7ce74-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce74-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce74-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce74-126">입력</span><span class="sxs-lookup"><span data-stu-id="7ce74-126">INPUTS</span></span>

## <span data-ttu-id="7ce74-127">출력</span><span class="sxs-lookup"><span data-stu-id="7ce74-127">OUTPUTS</span></span>

## <span data-ttu-id="7ce74-128">상속자</span><span class="sxs-lookup"><span data-stu-id="7ce74-128">NOTES</span></span>

## <span data-ttu-id="7ce74-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ce74-129">RELATED LINKS</span></span>

[<span data-ttu-id="7ce74-130">Azure Site Recovery 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ce74-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


