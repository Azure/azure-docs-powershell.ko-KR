---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491481"
---
# <span data-ttu-id="b19a3-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="b19a3-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="b19a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b19a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b19a3-103">Azure 웹앱 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="b19a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="b19a3-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b19a3-105">설명</span><span class="sxs-lookup"><span data-stu-id="b19a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b19a3-106">**Get-AzWebAppCertificate** cmdlet은 지정된 리소스 그룹과 연결된 Azure Web App 인증서에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="b19a3-107">인증서 지문을 알고 있는 경우 이 cmdlet을 사용하여 지정된 인증서에 대한 정보를 얻을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="b19a3-108">예제</span><span class="sxs-lookup"><span data-stu-id="b19a3-108">EXAMPLES</span></span>

### <span data-ttu-id="b19a3-109">예제 1: 리소스 그룹에서 웹앱 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="b19a3-110">이 명령은 리소스 그룹 ContosoResourceGroup과 연결된 업로드된 웹앱 인증서에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="b19a3-111">예제 2: 지정된 웹앱 인증서를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="b19a3-112">이 명령은 지문 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3을 사용하여 ContosoResourceGroup 웹앱 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="b19a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b19a3-113">PARAMETERS</span></span>

### <span data-ttu-id="b19a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b19a3-114">-DefaultProfile</span></span>
<span data-ttu-id="b19a3-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b19a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="b19a3-117">인증서가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="b19a3-118">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b19a3-118">-Thumbprint</span></span>
<span data-ttu-id="b19a3-119">인증서에 대한 고유 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="b19a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19a3-120">CommonParameters</span></span>
<span data-ttu-id="b19a3-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b19a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19a3-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b19a3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19a3-123">입력</span><span class="sxs-lookup"><span data-stu-id="b19a3-123">INPUTS</span></span>

### <span data-ttu-id="b19a3-124">없음</span><span class="sxs-lookup"><span data-stu-id="b19a3-124">None</span></span>

## <span data-ttu-id="b19a3-125">출력</span><span class="sxs-lookup"><span data-stu-id="b19a3-125">OUTPUTS</span></span>

### <span data-ttu-id="b19a3-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="b19a3-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="b19a3-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b19a3-127">NOTES</span></span>

## <span data-ttu-id="b19a3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b19a3-128">RELATED LINKS</span></span>

[<span data-ttu-id="b19a3-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b19a3-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


