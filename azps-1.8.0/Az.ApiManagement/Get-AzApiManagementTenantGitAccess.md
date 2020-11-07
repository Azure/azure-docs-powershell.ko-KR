---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 2fe14349b179634bf93050840271d4d4b6905b3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689126"
---
# <span data-ttu-id="7a863-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="7a863-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="7a863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a863-102">SYNOPSIS</span></span>
<span data-ttu-id="7a863-103">테 넌 트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a863-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="7a863-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a863-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a863-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a863-105">DESCRIPTION</span></span>
<span data-ttu-id="7a863-106">**AzApiManagementTenantGitAccess** cmdlet은 테 넌 트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a863-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="7a863-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a863-107">EXAMPLES</span></span>

### <span data-ttu-id="7a863-108">예제 1: 테 넌 트 액세스 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="7a863-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="7a863-109">이 명령은 지정 된 컨텍스트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a863-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="7a863-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a863-110">PARAMETERS</span></span>

### <span data-ttu-id="7a863-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7a863-111">-Context</span></span>
<span data-ttu-id="7a863-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a863-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a863-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a863-113">-DefaultProfile</span></span>
<span data-ttu-id="7a863-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a863-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a863-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a863-115">CommonParameters</span></span>
<span data-ttu-id="7a863-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a863-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a863-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a863-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a863-118">입력</span><span class="sxs-lookup"><span data-stu-id="7a863-118">INPUTS</span></span>

### <span data-ttu-id="7a863-119">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7a863-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="7a863-120">출력</span><span class="sxs-lookup"><span data-stu-id="7a863-120">OUTPUTS</span></span>

### <span data-ttu-id="7a863-121">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="7a863-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="7a863-122">상속자</span><span class="sxs-lookup"><span data-stu-id="7a863-122">NOTES</span></span>

## <span data-ttu-id="7a863-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a863-123">RELATED LINKS</span></span>