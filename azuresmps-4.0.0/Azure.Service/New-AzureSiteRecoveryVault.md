---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045974"
---
# <span data-ttu-id="93a14-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="93a14-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="93a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93a14-102">SYNOPSIS</span></span>
<span data-ttu-id="93a14-103">사이트 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="93a14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93a14-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93a14-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93a14-105">DESCRIPTION</span></span>
<span data-ttu-id="93a14-106">**AzureSiteRecoveryVault** Cmdlet은 Azure Site Recovery 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="93a14-107">예제의</span><span class="sxs-lookup"><span data-stu-id="93a14-107">EXAMPLES</span></span>

### <span data-ttu-id="93a14-108">예제 1: 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="93a14-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="93a14-109">이 명령은 US 위치에 ContosoVault 이라는 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="93a14-110">변수</span><span class="sxs-lookup"><span data-stu-id="93a14-110">PARAMETERS</span></span>

### <span data-ttu-id="93a14-111">-위치</span><span class="sxs-lookup"><span data-stu-id="93a14-111">-Location</span></span>
<span data-ttu-id="93a14-112">지리적 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-112">Specifies the geographical location.</span></span>

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

### <span data-ttu-id="93a14-113">-이름</span><span class="sxs-lookup"><span data-stu-id="93a14-113">-Name</span></span>
<span data-ttu-id="93a14-114">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="93a14-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="93a14-115">-Profile</span></span>
<span data-ttu-id="93a14-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93a14-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93a14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a14-118">CommonParameters</span></span>
<span data-ttu-id="93a14-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93a14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a14-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a14-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a14-121">입력</span><span class="sxs-lookup"><span data-stu-id="93a14-121">INPUTS</span></span>

## <span data-ttu-id="93a14-122">출력</span><span class="sxs-lookup"><span data-stu-id="93a14-122">OUTPUTS</span></span>

## <span data-ttu-id="93a14-123">상속자</span><span class="sxs-lookup"><span data-stu-id="93a14-123">NOTES</span></span>

## <span data-ttu-id="93a14-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93a14-124">RELATED LINKS</span></span>

[<span data-ttu-id="93a14-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="93a14-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


