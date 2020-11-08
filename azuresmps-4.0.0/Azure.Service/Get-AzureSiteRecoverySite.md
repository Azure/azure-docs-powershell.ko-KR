---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045577"
---
# <span data-ttu-id="b6f90-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b6f90-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="b6f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f90-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f90-103">사이트 복구 자격 증명 모음에서 Hyper-v 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="b6f90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6f90-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6f90-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6f90-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f90-106">**AzureSiteRecoverySite** Cmdlet은 Azure Site Recovery 자격 증명 모음에서 hyper-v 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b6f90-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b6f90-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f90-108">예제 1: 복구 사이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f90-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="b6f90-109">이 명령은 현재 자격 증명 모음에 대 한 복구 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="b6f90-110">변수</span><span class="sxs-lookup"><span data-stu-id="b6f90-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f90-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="b6f90-111">-Profile</span></span>
<span data-ttu-id="b6f90-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6f90-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6f90-114">-저장실</span><span class="sxs-lookup"><span data-stu-id="b6f90-114">-Vault</span></span>
<span data-ttu-id="b6f90-115">사이트를 가져올 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="b6f90-116">**Asrvault** 개체를 얻으려면 **Get-AzureSiteRecoveryVault** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="b6f90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f90-117">CommonParameters</span></span>
<span data-ttu-id="b6f90-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f90-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f90-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f90-120">입력</span><span class="sxs-lookup"><span data-stu-id="b6f90-120">INPUTS</span></span>

## <span data-ttu-id="b6f90-121">출력</span><span class="sxs-lookup"><span data-stu-id="b6f90-121">OUTPUTS</span></span>

## <span data-ttu-id="b6f90-122">상속자</span><span class="sxs-lookup"><span data-stu-id="b6f90-122">NOTES</span></span>

## <span data-ttu-id="b6f90-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6f90-123">RELATED LINKS</span></span>

[<span data-ttu-id="b6f90-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b6f90-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="b6f90-125">새로운 AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b6f90-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


