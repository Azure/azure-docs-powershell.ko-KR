---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702684"
---
# <span data-ttu-id="853ff-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="853ff-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="853ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="853ff-102">SYNOPSIS</span></span>
<span data-ttu-id="853ff-103">사이트 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="853ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="853ff-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="853ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="853ff-105">DESCRIPTION</span></span>
<span data-ttu-id="853ff-106">**AzureRmSiteRecoveryVault** Cmdlet은 Azure Site Recovery 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="853ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="853ff-107">EXAMPLES</span></span>

## <span data-ttu-id="853ff-108">변수</span><span class="sxs-lookup"><span data-stu-id="853ff-108">PARAMETERS</span></span>

### <span data-ttu-id="853ff-109">-위치</span><span class="sxs-lookup"><span data-stu-id="853ff-109">-Location</span></span>
<span data-ttu-id="853ff-110">지리적 위치 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853ff-111">-이름</span><span class="sxs-lookup"><span data-stu-id="853ff-111">-Name</span></span>
<span data-ttu-id="853ff-112">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853ff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="853ff-113">-ResourceGroupName</span></span>
<span data-ttu-id="853ff-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="853ff-115">-DefaultProfile</span></span>
<span data-ttu-id="853ff-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="853ff-117">CommonParameters</span></span>
<span data-ttu-id="853ff-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="853ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="853ff-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="853ff-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="853ff-120">입력</span><span class="sxs-lookup"><span data-stu-id="853ff-120">INPUTS</span></span>

## <span data-ttu-id="853ff-121">출력</span><span class="sxs-lookup"><span data-stu-id="853ff-121">OUTPUTS</span></span>

## <span data-ttu-id="853ff-122">상속자</span><span class="sxs-lookup"><span data-stu-id="853ff-122">NOTES</span></span>

## <span data-ttu-id="853ff-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="853ff-123">RELATED LINKS</span></span>

[<span data-ttu-id="853ff-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="853ff-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="853ff-125">제거-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="853ff-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
