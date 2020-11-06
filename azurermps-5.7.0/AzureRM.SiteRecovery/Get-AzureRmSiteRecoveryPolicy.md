---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526564"
---
# <span data-ttu-id="f6060-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f6060-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="f6060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6060-102">SYNOPSIS</span></span>
<span data-ttu-id="f6060-103">사이트 복구 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6060-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6060-104">SYNTAX</span></span>

### <span data-ttu-id="f6060-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6060-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6060-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f6060-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6060-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f6060-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6060-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f6060-108">DESCRIPTION</span></span>
<span data-ttu-id="f6060-109">**AzureRmSiteRecoveryPolicy** cmdlet은 구성 된 Azure Site Recovery 보호 정책 또는 이름에 따른 특정 보호 정책의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="f6060-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f6060-110">EXAMPLES</span></span>

## <span data-ttu-id="f6060-111">변수</span><span class="sxs-lookup"><span data-stu-id="f6060-111">PARAMETERS</span></span>

### <span data-ttu-id="f6060-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6060-112">-DefaultProfile</span></span>
<span data-ttu-id="f6060-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6060-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f6060-114">-FriendlyName</span></span>
<span data-ttu-id="f6060-115">사이트 복구 복제 정책의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6060-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f6060-116">-Name</span></span>
<span data-ttu-id="f6060-117">사이트 복구 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-117">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="f6060-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6060-118">CommonParameters</span></span>
<span data-ttu-id="f6060-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6060-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6060-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6060-121">입력</span><span class="sxs-lookup"><span data-stu-id="f6060-121">INPUTS</span></span>

### <span data-ttu-id="f6060-122">않아야</span><span class="sxs-lookup"><span data-stu-id="f6060-122">None</span></span>
<span data-ttu-id="f6060-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6060-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6060-124">출력</span><span class="sxs-lookup"><span data-stu-id="f6060-124">OUTPUTS</span></span>

### <span data-ttu-id="f6060-125">System.webserver. t e r ' 1 [SiteRecovery Rr 정책]</span><span class="sxs-lookup"><span data-stu-id="f6060-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="f6060-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f6060-126">NOTES</span></span>

## <span data-ttu-id="f6060-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6060-127">RELATED LINKS</span></span>

[<span data-ttu-id="f6060-128">새로운 AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f6060-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="f6060-129">제거-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f6060-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
