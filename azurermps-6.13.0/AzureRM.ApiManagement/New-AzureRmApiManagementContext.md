---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 56dc320ea6aafd37e93912071a3256040342e2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533487"
---
# <span data-ttu-id="91263-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91263-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="91263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91263-102">SYNOPSIS</span></span>
<span data-ttu-id="91263-103">PsAzureApiManagementContext의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91263-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91263-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91263-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91263-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91263-105">DESCRIPTION</span></span>
<span data-ttu-id="91263-106">**AzureRmApiManagementContext** Cmdlet은 **PsAzureApiManagementContext** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91263-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="91263-107">컨텍스트는 모든 API Management 서비스 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91263-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="91263-108">예제의</span><span class="sxs-lookup"><span data-stu-id="91263-108">EXAMPLES</span></span>

### <span data-ttu-id="91263-109">예제 1: PsApiManagementContext 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="91263-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="91263-110">이 명령은 **PsApiManagementContext** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91263-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="91263-111">변수</span><span class="sxs-lookup"><span data-stu-id="91263-111">PARAMETERS</span></span>

### <span data-ttu-id="91263-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91263-112">-DefaultProfile</span></span>
<span data-ttu-id="91263-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91263-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91263-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91263-114">-ResourceGroupName</span></span>
<span data-ttu-id="91263-115">API Management 서비스를 배포 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91263-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91263-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="91263-116">-ServiceName</span></span>
<span data-ttu-id="91263-117">배포 된 API Management 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91263-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91263-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91263-118">CommonParameters</span></span>
<span data-ttu-id="91263-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91263-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91263-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91263-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91263-121">입력</span><span class="sxs-lookup"><span data-stu-id="91263-121">INPUTS</span></span>

### <span data-ttu-id="91263-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91263-122">System.String</span></span>

## <span data-ttu-id="91263-123">출력</span><span class="sxs-lookup"><span data-stu-id="91263-123">OUTPUTS</span></span>

### <span data-ttu-id="91263-124">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91263-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="91263-125">상속자</span><span class="sxs-lookup"><span data-stu-id="91263-125">NOTES</span></span>

## <span data-ttu-id="91263-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91263-126">RELATED LINKS</span></span>
