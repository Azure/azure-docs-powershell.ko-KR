---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045892"
---
# <span data-ttu-id="654f8-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="654f8-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="654f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="654f8-102">SYNOPSIS</span></span>
<span data-ttu-id="654f8-103">사이트 복구 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="654f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="654f8-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="654f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="654f8-105">DESCRIPTION</span></span>
<span data-ttu-id="654f8-106">**AzureSiteRecoverySite** cmdlet은 현재 자격 증명 모음에 Azure site Recovery 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="654f8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="654f8-107">EXAMPLES</span></span>

### <span data-ttu-id="654f8-108">예제 1: 사이트 복구 사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="654f8-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="654f8-109">이 명령은 RecoverySite07 이라는 사이트 복구 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="654f8-110">변수</span><span class="sxs-lookup"><span data-stu-id="654f8-110">PARAMETERS</span></span>

### <span data-ttu-id="654f8-111">-이름</span><span class="sxs-lookup"><span data-stu-id="654f8-111">-Name</span></span>
<span data-ttu-id="654f8-112">사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654f8-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="654f8-113">-Profile</span></span>
<span data-ttu-id="654f8-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="654f8-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="654f8-116">-저장실</span><span class="sxs-lookup"><span data-stu-id="654f8-116">-Vault</span></span>
<span data-ttu-id="654f8-117">사이트를 만들 보관소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="654f8-118">**Asrvault** 개체를 얻으려면 **Get-AzureSiteRecoveryVault** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654f8-119">CommonParameters</span></span>
<span data-ttu-id="654f8-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="654f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654f8-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654f8-122">입력</span><span class="sxs-lookup"><span data-stu-id="654f8-122">INPUTS</span></span>

## <span data-ttu-id="654f8-123">출력</span><span class="sxs-lookup"><span data-stu-id="654f8-123">OUTPUTS</span></span>

## <span data-ttu-id="654f8-124">상속자</span><span class="sxs-lookup"><span data-stu-id="654f8-124">NOTES</span></span>

## <span data-ttu-id="654f8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="654f8-125">RELATED LINKS</span></span>

[<span data-ttu-id="654f8-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="654f8-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="654f8-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="654f8-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


