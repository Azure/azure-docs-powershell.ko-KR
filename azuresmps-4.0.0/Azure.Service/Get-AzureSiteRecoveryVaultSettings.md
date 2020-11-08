---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046566"
---
# <span data-ttu-id="93c6a-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="93c6a-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="93c6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="93c6a-103">사이트 복구 자격 증명 모음에 대 한 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93c6a-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="93c6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93c6a-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93c6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="93c6a-106">**Get-AzureSiteRecoveryVaultSettings** cmdlet은 현재 Azure Site Recovery 자격 증명 모음과 관련 된 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93c6a-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="93c6a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="93c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="93c6a-108">예제 1: 설정 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="93c6a-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="93c6a-109">이 명령은 현재 Azure Site Recovery 자격 증명 모음에 대 한 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93c6a-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="93c6a-110">변수</span><span class="sxs-lookup"><span data-stu-id="93c6a-110">PARAMETERS</span></span>

### <span data-ttu-id="93c6a-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="93c6a-111">-Profile</span></span>
<span data-ttu-id="93c6a-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c6a-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93c6a-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="93c6a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93c6a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c6a-114">CommonParameters</span></span>
<span data-ttu-id="93c6a-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c6a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c6a-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c6a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c6a-117">입력</span><span class="sxs-lookup"><span data-stu-id="93c6a-117">INPUTS</span></span>

## <span data-ttu-id="93c6a-118">출력</span><span class="sxs-lookup"><span data-stu-id="93c6a-118">OUTPUTS</span></span>

## <span data-ttu-id="93c6a-119">상속자</span><span class="sxs-lookup"><span data-stu-id="93c6a-119">NOTES</span></span>

## <span data-ttu-id="93c6a-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93c6a-120">RELATED LINKS</span></span>

[<span data-ttu-id="93c6a-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="93c6a-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="93c6a-122">가져오기-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="93c6a-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


