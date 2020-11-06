---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532903"
---
# <span data-ttu-id="69fd8-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="69fd8-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="69fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="69fd8-103">사이트 복구 서버를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="69fd8-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69fd8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69fd8-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69fd8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69fd8-105">DESCRIPTION</span></span>
<span data-ttu-id="69fd8-106">**업데이트 AzureRmSiteRecoveryServer** Cmdlet은 Azure Site Recovery 서버를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="69fd8-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="69fd8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69fd8-107">EXAMPLES</span></span>

## <span data-ttu-id="69fd8-108">변수</span><span class="sxs-lookup"><span data-stu-id="69fd8-108">PARAMETERS</span></span>

### <span data-ttu-id="69fd8-109">-서버</span><span class="sxs-lookup"><span data-stu-id="69fd8-109">-Server</span></span>
<span data-ttu-id="69fd8-110">이 cmdlet이 업데이트 하는 사이트 복구 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69fd8-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69fd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fd8-111">-DefaultProfile</span></span>
<span data-ttu-id="69fd8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69fd8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69fd8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fd8-113">CommonParameters</span></span>
<span data-ttu-id="69fd8-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69fd8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fd8-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69fd8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fd8-116">입력</span><span class="sxs-lookup"><span data-stu-id="69fd8-116">INPUTS</span></span>

### <span data-ttu-id="69fd8-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="69fd8-117">ASRServer</span></span>
<span data-ttu-id="69fd8-118">' Server ' 매개 변수는 파이프라인에서 ' ASRServer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69fd8-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="69fd8-119">출력</span><span class="sxs-lookup"><span data-stu-id="69fd8-119">OUTPUTS</span></span>

## <span data-ttu-id="69fd8-120">상속자</span><span class="sxs-lookup"><span data-stu-id="69fd8-120">NOTES</span></span>

## <span data-ttu-id="69fd8-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69fd8-121">RELATED LINKS</span></span>

[<span data-ttu-id="69fd8-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="69fd8-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="69fd8-123">제거-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="69fd8-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
