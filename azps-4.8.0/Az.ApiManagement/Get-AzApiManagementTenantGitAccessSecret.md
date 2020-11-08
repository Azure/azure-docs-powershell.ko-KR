---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056842"
---
# <span data-ttu-id="fd504-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="fd504-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="fd504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd504-102">SYNOPSIS</span></span>
<span data-ttu-id="fd504-103">테 넌 트에 대 한 Git 액세스 구성 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="fd504-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd504-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd504-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd504-105">DESCRIPTION</span></span>
<span data-ttu-id="fd504-106">테 넌 트에 대 한 Git 액세스 구성 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="fd504-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fd504-107">EXAMPLES</span></span>

### <span data-ttu-id="fd504-108">예제 1: 테 넌 트 액세스 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="fd504-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="fd504-109">이 명령은 지정 된 컨텍스트에 대 한 Git 액세스 구성 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="fd504-110">변수</span><span class="sxs-lookup"><span data-stu-id="fd504-110">PARAMETERS</span></span>

### <span data-ttu-id="fd504-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fd504-111">-Context</span></span>
<span data-ttu-id="fd504-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd504-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd504-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd504-114">-DefaultProfile</span></span>
<span data-ttu-id="fd504-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd504-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd504-116">CommonParameters</span></span>
<span data-ttu-id="fd504-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd504-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd504-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fd504-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd504-119">입력</span><span class="sxs-lookup"><span data-stu-id="fd504-119">INPUTS</span></span>

### <span data-ttu-id="fd504-120">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd504-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="fd504-121">출력</span><span class="sxs-lookup"><span data-stu-id="fd504-121">OUTPUTS</span></span>

### <span data-ttu-id="fd504-122">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="fd504-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="fd504-123">상속자</span><span class="sxs-lookup"><span data-stu-id="fd504-123">NOTES</span></span>

## <span data-ttu-id="fd504-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd504-124">RELATED LINKS</span></span>
