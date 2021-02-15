---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182433"
---
# <span data-ttu-id="a8a08-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a8a08-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="a8a08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a08-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a08-103">Azure Web App에 대한 App Service 관리 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="a8a08-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8a08-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8a08-105">설명</span><span class="sxs-lookup"><span data-stu-id="a8a08-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a08-106">**Remove-AzWebAppCertificate** cmdlet은 Azure App Service 관리 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="a8a08-107">예제</span><span class="sxs-lookup"><span data-stu-id="a8a08-107">EXAMPLES</span></span>

### <span data-ttu-id="a8a08-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8a08-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="a8a08-109">이 명령은 주어진 웹앱에 대한 App Service 관리 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="a8a08-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8a08-110">PARAMETERS</span></span>

### <span data-ttu-id="a8a08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a08-111">-DefaultProfile</span></span>
<span data-ttu-id="a8a08-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a08-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a08-113">-ResourceGroupName</span></span>
<span data-ttu-id="a8a08-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a08-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="a8a08-115">-ThumbPrint</span></span>
<span data-ttu-id="a8a08-116">웹 공간에 이미 있는 인증서의 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a08-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a08-117">CommonParameters</span></span>
<span data-ttu-id="a8a08-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a08-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a08-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8a08-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a08-120">입력</span><span class="sxs-lookup"><span data-stu-id="a8a08-120">INPUTS</span></span>

### <span data-ttu-id="a8a08-121">없음</span><span class="sxs-lookup"><span data-stu-id="a8a08-121">None</span></span>

## <span data-ttu-id="a8a08-122">출력</span><span class="sxs-lookup"><span data-stu-id="a8a08-122">OUTPUTS</span></span>

### <span data-ttu-id="a8a08-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="a8a08-123">System.Void</span></span>

## <span data-ttu-id="a8a08-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8a08-124">NOTES</span></span>

## <span data-ttu-id="a8a08-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8a08-125">RELATED LINKS</span></span>
[<span data-ttu-id="a8a08-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a8a08-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
