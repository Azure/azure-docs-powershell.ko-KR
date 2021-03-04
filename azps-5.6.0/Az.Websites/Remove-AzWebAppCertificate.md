---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981723"
---
# <span data-ttu-id="56c4d-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="56c4d-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="56c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="56c4d-103">Azure Web App에 대한 App Service 관리 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-103">Removes an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="56c4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="56c4d-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56c4d-105">설명</span><span class="sxs-lookup"><span data-stu-id="56c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="56c4d-106">**Remove-AzWebAppCertificate** cmdlet은 Azure App Service 관리 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-106">The **Remove-AzWebAppCertificate** cmdlet Removes an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="56c4d-107">예제</span><span class="sxs-lookup"><span data-stu-id="56c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="56c4d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="56c4d-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="56c4d-109">이 명령은 주어진 웹앱에 대한 App Service 관리 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="56c4d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56c4d-110">PARAMETERS</span></span>

### <span data-ttu-id="56c4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c4d-111">-DefaultProfile</span></span>
<span data-ttu-id="56c4d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c4d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c4d-113">-ResourceGroupName</span></span>
<span data-ttu-id="56c4d-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="56c4d-115">-지문</span><span class="sxs-lookup"><span data-stu-id="56c4d-115">-ThumbPrint</span></span>
<span data-ttu-id="56c4d-116">웹 공간에 이미 있는 인증서의 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-116">Thumbprint of the certificate that already exists in web space.</span></span>

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

### <span data-ttu-id="56c4d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c4d-117">CommonParameters</span></span>
<span data-ttu-id="56c4d-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56c4d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c4d-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56c4d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c4d-120">입력</span><span class="sxs-lookup"><span data-stu-id="56c4d-120">INPUTS</span></span>

### <span data-ttu-id="56c4d-121">없음</span><span class="sxs-lookup"><span data-stu-id="56c4d-121">None</span></span>

## <span data-ttu-id="56c4d-122">출력</span><span class="sxs-lookup"><span data-stu-id="56c4d-122">OUTPUTS</span></span>

### <span data-ttu-id="56c4d-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="56c4d-123">System.Void</span></span>

## <span data-ttu-id="56c4d-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56c4d-124">NOTES</span></span>

## <span data-ttu-id="56c4d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56c4d-125">RELATED LINKS</span></span>
[<span data-ttu-id="56c4d-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="56c4d-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
