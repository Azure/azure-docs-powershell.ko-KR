---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004875"
---
# <span data-ttu-id="68392-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="68392-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="68392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68392-102">SYNOPSIS</span></span>
<span data-ttu-id="68392-103">테넌트에 대한 Git 액세스 구성 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68392-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="68392-104">구문</span><span class="sxs-lookup"><span data-stu-id="68392-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68392-105">설명</span><span class="sxs-lookup"><span data-stu-id="68392-105">DESCRIPTION</span></span>
<span data-ttu-id="68392-106">테넌트에 대한 Git 액세스 구성 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68392-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="68392-107">예제</span><span class="sxs-lookup"><span data-stu-id="68392-107">EXAMPLES</span></span>

### <span data-ttu-id="68392-108">예제 1: 테넌트 액세스 구성 얻기</span><span class="sxs-lookup"><span data-stu-id="68392-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="68392-109">이 명령은 지정된 컨텍스트에 대한 Git 액세스 구성 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68392-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="68392-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68392-110">PARAMETERS</span></span>

### <span data-ttu-id="68392-111">-Context</span><span class="sxs-lookup"><span data-stu-id="68392-111">-Context</span></span>
<span data-ttu-id="68392-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="68392-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68392-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68392-113">This parameter is required.</span></span>

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

### <span data-ttu-id="68392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68392-114">-DefaultProfile</span></span>
<span data-ttu-id="68392-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68392-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68392-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68392-116">CommonParameters</span></span>
<span data-ttu-id="68392-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68392-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68392-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68392-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68392-119">입력</span><span class="sxs-lookup"><span data-stu-id="68392-119">INPUTS</span></span>

### <span data-ttu-id="68392-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68392-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="68392-121">출력</span><span class="sxs-lookup"><span data-stu-id="68392-121">OUTPUTS</span></span>

### <span data-ttu-id="68392-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="68392-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="68392-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68392-123">NOTES</span></span>

## <span data-ttu-id="68392-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68392-124">RELATED LINKS</span></span>
