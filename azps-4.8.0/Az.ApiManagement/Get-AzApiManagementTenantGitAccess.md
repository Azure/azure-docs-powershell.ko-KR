---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049258"
---
# <span data-ttu-id="b21dc-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="b21dc-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="b21dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b21dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b21dc-103">테 넌 트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="b21dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b21dc-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b21dc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b21dc-105">DESCRIPTION</span></span>
<span data-ttu-id="b21dc-106">**AzApiManagementTenantGitAccess** cmdlet은 테 넌 트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="b21dc-107">키가 결과 세부 정보에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-107">Keys will not be included into result details.</span></span> <span data-ttu-id="b21dc-108">클라이언트 비밀을 가져오려면 Get-help를 **AzApiManagementTenantGitAccessSecret** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="b21dc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b21dc-109">EXAMPLES</span></span>

### <span data-ttu-id="b21dc-110">예제 1: 테 넌 트 액세스 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b21dc-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="b21dc-111">이 명령은 지정 된 컨텍스트에 대 한 Git 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="b21dc-112">변수</span><span class="sxs-lookup"><span data-stu-id="b21dc-112">PARAMETERS</span></span>

### <span data-ttu-id="b21dc-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b21dc-113">-Context</span></span>
<span data-ttu-id="b21dc-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b21dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21dc-115">-DefaultProfile</span></span>
<span data-ttu-id="b21dc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b21dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21dc-117">CommonParameters</span></span>
<span data-ttu-id="b21dc-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21dc-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b21dc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21dc-120">입력</span><span class="sxs-lookup"><span data-stu-id="b21dc-120">INPUTS</span></span>

### <span data-ttu-id="b21dc-121">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b21dc-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b21dc-122">출력</span><span class="sxs-lookup"><span data-stu-id="b21dc-122">OUTPUTS</span></span>

### <span data-ttu-id="b21dc-123">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b21dc-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b21dc-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b21dc-124">NOTES</span></span>

## <span data-ttu-id="b21dc-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b21dc-125">RELATED LINKS</span></span>
