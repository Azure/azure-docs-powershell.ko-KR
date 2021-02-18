---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405825"
---
# <span data-ttu-id="8060b-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8060b-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="8060b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8060b-102">SYNOPSIS</span></span>
<span data-ttu-id="8060b-103">Site Recovery 자격 증명 모음에 대한 보호 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="8060b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8060b-104">SYNTAX</span></span>

### <span data-ttu-id="8060b-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="8060b-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8060b-106">ById</span><span class="sxs-lookup"><span data-stu-id="8060b-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8060b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8060b-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8060b-108">설명</span><span class="sxs-lookup"><span data-stu-id="8060b-108">DESCRIPTION</span></span>
<span data-ttu-id="8060b-109">**Get-AzureSiteRecoveryProtectionContainer** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대한 보호 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="8060b-110">보호 컨테이너는 가상 머신과 같은 보호된 개체에 대한 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="8060b-111">보호 정책은 보호된 항목에 대한 복제 설정을 정의하며 보호 컨테이너와 연결하여 보호된 엔터티에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="8060b-112">예제</span><span class="sxs-lookup"><span data-stu-id="8060b-112">EXAMPLES</span></span>

### <span data-ttu-id="8060b-113">예제 1: 보호된 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-113">Example 1: Get protected containers</span></span>
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

<span data-ttu-id="8060b-114">이 명령은 현재 자격 증명 모음에 대해 보호된 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="8060b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8060b-115">PARAMETERS</span></span>

### <span data-ttu-id="8060b-116">-Id</span><span class="sxs-lookup"><span data-stu-id="8060b-116">-Id</span></span>
<span data-ttu-id="8060b-117">보호된 컨테이너의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="8060b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8060b-118">-Name</span></span>
<span data-ttu-id="8060b-119">얻을 보호 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="8060b-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="8060b-120">-Profile</span></span>
<span data-ttu-id="8060b-121">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8060b-122">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8060b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8060b-123">CommonParameters</span></span>
<span data-ttu-id="8060b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8060b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8060b-125">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8060b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8060b-126">입력</span><span class="sxs-lookup"><span data-stu-id="8060b-126">INPUTS</span></span>

## <span data-ttu-id="8060b-127">출력</span><span class="sxs-lookup"><span data-stu-id="8060b-127">OUTPUTS</span></span>

## <span data-ttu-id="8060b-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8060b-128">NOTES</span></span>

## <span data-ttu-id="8060b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8060b-129">RELATED LINKS</span></span>




