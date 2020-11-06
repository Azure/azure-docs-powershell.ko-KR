---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: 94cd9c6aa3c47d87b1c99a1f8ae68c48c613aefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529315"
---
# <span data-ttu-id="60009-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="60009-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="60009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60009-102">SYNOPSIS</span></span>
<span data-ttu-id="60009-103">Azure Web App 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60009-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60009-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60009-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60009-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60009-105">DESCRIPTION</span></span>
<span data-ttu-id="60009-106">**AzureRmWebAppCertificate** cmdlet은 지정 된 리소스 그룹과 연결 된 Azure Web App 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60009-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="60009-107">인증서 지문을 알면이 cmdlet을 사용 하 여 지정 된 인증서에 대 한 정보를 얻을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60009-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="60009-108">예제의</span><span class="sxs-lookup"><span data-stu-id="60009-108">EXAMPLES</span></span>

### <span data-ttu-id="60009-109">예제 1: 리소스 그룹에서 웹 앱 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="60009-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="60009-110">이 명령은 리소스 그룹 ContosoResourceGroup와 연결 된 업로드 된 웹 앱 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="60009-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="60009-111">예제 2: 지정 된 웹 앱 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="60009-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="60009-112">이 명령은 지문 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3를 사용 하 여 ContosoResourceGroup Web App 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60009-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="60009-113">변수</span><span class="sxs-lookup"><span data-stu-id="60009-113">PARAMETERS</span></span>

### <span data-ttu-id="60009-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60009-114">-DefaultProfile</span></span>
<span data-ttu-id="60009-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60009-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60009-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60009-116">-ResourceGroupName</span></span>
<span data-ttu-id="60009-117">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60009-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60009-118">-지문</span><span class="sxs-lookup"><span data-stu-id="60009-118">-Thumbprint</span></span>
<span data-ttu-id="60009-119">인증서에 대 한 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60009-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60009-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60009-120">CommonParameters</span></span>
<span data-ttu-id="60009-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60009-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60009-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60009-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60009-123">입력</span><span class="sxs-lookup"><span data-stu-id="60009-123">INPUTS</span></span>

### <span data-ttu-id="60009-124">않아야</span><span class="sxs-lookup"><span data-stu-id="60009-124">None</span></span>

## <span data-ttu-id="60009-125">출력</span><span class="sxs-lookup"><span data-stu-id="60009-125">OUTPUTS</span></span>

### <span data-ttu-id="60009-126">Microsoft. Azure. 관리자. 인증서</span><span class="sxs-lookup"><span data-stu-id="60009-126">Microsoft.Azure.Management.WebSites.Models.Certificate</span></span>

## <span data-ttu-id="60009-127">상속자</span><span class="sxs-lookup"><span data-stu-id="60009-127">NOTES</span></span>

## <span data-ttu-id="60009-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60009-128">RELATED LINKS</span></span>

[<span data-ttu-id="60009-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="60009-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


