---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 29e15515dfb5c8db53255cd283573fec11239940
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004891"
---
# <span data-ttu-id="3e1ef-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="3e1ef-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="3e1ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1ef-103">테넌트에 대한 Git 액세스 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="3e1ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e1ef-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1ef-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e1ef-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1ef-106">**Get-AzApiManagementTenantGitAccess** cmdlet은 테넌트에 대한 Git 액세스 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="3e1ef-107">키는 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-107">Keys will not be included into result details.</span></span> <span data-ttu-id="3e1ef-108">클라이언트 비밀을 얻기 위해 **Get-AzApiManagementTenantGitAccessSecret** 을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="3e1ef-109">예제</span><span class="sxs-lookup"><span data-stu-id="3e1ef-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1ef-110">예제 1: 테넌트 액세스 구성 얻기</span><span class="sxs-lookup"><span data-stu-id="3e1ef-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="3e1ef-111">이 명령은 지정된 컨텍스트에 대한 Git 액세스 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="3e1ef-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3e1ef-112">PARAMETERS</span></span>

### <span data-ttu-id="3e1ef-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3e1ef-113">-Context</span></span>
<span data-ttu-id="3e1ef-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="3e1ef-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3e1ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1ef-115">-DefaultProfile</span></span>
<span data-ttu-id="3e1ef-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e1ef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1ef-117">CommonParameters</span></span>
<span data-ttu-id="3e1ef-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e1ef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1ef-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e1ef-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1ef-120">입력</span><span class="sxs-lookup"><span data-stu-id="3e1ef-120">INPUTS</span></span>

### <span data-ttu-id="3e1ef-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e1ef-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3e1ef-122">출력</span><span class="sxs-lookup"><span data-stu-id="3e1ef-122">OUTPUTS</span></span>

### <span data-ttu-id="3e1ef-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3e1ef-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3e1ef-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e1ef-124">NOTES</span></span>

## <span data-ttu-id="3e1ef-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e1ef-125">RELATED LINKS</span></span>
