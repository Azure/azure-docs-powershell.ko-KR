---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710938"
---
# <span data-ttu-id="fabf8-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="fabf8-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="fabf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabf8-102">SYNOPSIS</span></span>
<span data-ttu-id="fabf8-103">현재 자격 증명 모음에 등록 된 사이트 복구 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fabf8-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fabf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fabf8-104">SYNTAX</span></span>

### <span data-ttu-id="fabf8-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fabf8-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabf8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fabf8-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabf8-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fabf8-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fabf8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fabf8-108">DESCRIPTION</span></span>
<span data-ttu-id="fabf8-109">**AzureRmSiteRecoveryServer** cmdlet은 현재 사이트 복구 자격 증명 모음에 등록 된 Azure Site recovery 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fabf8-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="fabf8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fabf8-110">EXAMPLES</span></span>

## <span data-ttu-id="fabf8-111">변수</span><span class="sxs-lookup"><span data-stu-id="fabf8-111">PARAMETERS</span></span>

### <span data-ttu-id="fabf8-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fabf8-112">-FriendlyName</span></span>
<span data-ttu-id="fabf8-113">서버의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf8-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabf8-114">-이름</span><span class="sxs-lookup"><span data-stu-id="fabf8-114">-Name</span></span>
<span data-ttu-id="fabf8-115">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf8-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabf8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabf8-116">-DefaultProfile</span></span>
<span data-ttu-id="fabf8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fabf8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fabf8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabf8-118">CommonParameters</span></span>
<span data-ttu-id="fabf8-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabf8-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fabf8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabf8-121">입력</span><span class="sxs-lookup"><span data-stu-id="fabf8-121">INPUTS</span></span>

## <span data-ttu-id="fabf8-122">출력</span><span class="sxs-lookup"><span data-stu-id="fabf8-122">OUTPUTS</span></span>

### <span data-ttu-id="fabf8-123">System.webserver. t e r ' 1 [SiteRecovery], 또는.</span><span class="sxs-lookup"><span data-stu-id="fabf8-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="fabf8-124">상속자</span><span class="sxs-lookup"><span data-stu-id="fabf8-124">NOTES</span></span>

## <span data-ttu-id="fabf8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fabf8-125">RELATED LINKS</span></span>

[<span data-ttu-id="fabf8-126">제거-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="fabf8-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
