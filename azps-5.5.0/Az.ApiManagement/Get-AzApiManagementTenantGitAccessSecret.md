---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178108"
---
# <span data-ttu-id="fd4be-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="fd4be-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="fd4be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4be-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4be-103">테넌트에 대한 Git 액세스 구성 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="fd4be-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd4be-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd4be-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd4be-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4be-106">테넌트에 대한 Git 액세스 구성 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="fd4be-107">예제</span><span class="sxs-lookup"><span data-stu-id="fd4be-107">EXAMPLES</span></span>

### <span data-ttu-id="fd4be-108">예제 1: 테넌트 액세스 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="fd4be-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="fd4be-109">이 명령은 지정된 컨텍스트에 대한 Git 액세스 구성 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="fd4be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd4be-110">PARAMETERS</span></span>

### <span data-ttu-id="fd4be-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fd4be-111">-Context</span></span>
<span data-ttu-id="fd4be-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd4be-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fd4be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4be-114">-DefaultProfile</span></span>
<span data-ttu-id="fd4be-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd4be-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4be-116">CommonParameters</span></span>
<span data-ttu-id="fd4be-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4be-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4be-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd4be-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4be-119">입력</span><span class="sxs-lookup"><span data-stu-id="fd4be-119">INPUTS</span></span>

### <span data-ttu-id="fd4be-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd4be-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="fd4be-121">출력</span><span class="sxs-lookup"><span data-stu-id="fd4be-121">OUTPUTS</span></span>

### <span data-ttu-id="fd4be-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="fd4be-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="fd4be-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd4be-123">NOTES</span></span>

## <span data-ttu-id="fd4be-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd4be-124">RELATED LINKS</span></span>
