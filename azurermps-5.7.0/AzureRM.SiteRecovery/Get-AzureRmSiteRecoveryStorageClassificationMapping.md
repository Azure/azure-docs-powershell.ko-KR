---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703973"
---
# <span data-ttu-id="8ea06-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8ea06-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="8ea06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea06-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea06-103">사이트 복구에서 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ea06-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ea06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ea06-104">SYNTAX</span></span>

### <span data-ttu-id="8ea06-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ea06-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ea06-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ea06-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ea06-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8ea06-107">DESCRIPTION</span></span>
<span data-ttu-id="8ea06-108">**AzureRmSiteRecoveryStorageClassificationMapping** Cmdlet은 Azure Site Recovery에서 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ea06-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="8ea06-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8ea06-109">EXAMPLES</span></span>

## <span data-ttu-id="8ea06-110">변수</span><span class="sxs-lookup"><span data-stu-id="8ea06-110">PARAMETERS</span></span>

### <span data-ttu-id="8ea06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea06-111">-DefaultProfile</span></span>
<span data-ttu-id="8ea06-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ea06-113">-이름</span><span class="sxs-lookup"><span data-stu-id="8ea06-113">-Name</span></span>
<span data-ttu-id="8ea06-114">이 cmdlet이 가져오는 저장소 분류 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea06-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8ea06-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea06-115">CommonParameters</span></span>
<span data-ttu-id="8ea06-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea06-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea06-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea06-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea06-118">입력</span><span class="sxs-lookup"><span data-stu-id="8ea06-118">INPUTS</span></span>

### <span data-ttu-id="8ea06-119">않아야</span><span class="sxs-lookup"><span data-stu-id="8ea06-119">None</span></span>
<span data-ttu-id="8ea06-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea06-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ea06-121">출력</span><span class="sxs-lookup"><span data-stu-id="8ea06-121">OUTPUTS</span></span>

### <span data-ttu-id="8ea06-122">System.webserver. t e 1.aspx ' 1 [Microsoft SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="8ea06-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="8ea06-123">상속자</span><span class="sxs-lookup"><span data-stu-id="8ea06-123">NOTES</span></span>

## <span data-ttu-id="8ea06-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ea06-124">RELATED LINKS</span></span>

[<span data-ttu-id="8ea06-125">새로운 AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8ea06-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="8ea06-126">제거-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8ea06-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
