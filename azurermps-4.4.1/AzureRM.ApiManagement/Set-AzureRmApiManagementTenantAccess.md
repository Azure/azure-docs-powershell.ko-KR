---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525747"
---
# <span data-ttu-id="70b21-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="70b21-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="70b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70b21-102">SYNOPSIS</span></span>
<span data-ttu-id="70b21-103">테 넌 트 액세스를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70b21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70b21-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70b21-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70b21-105">DESCRIPTION</span></span>
<span data-ttu-id="70b21-106">**AzureRmApiManagementTenantAccess** cmdlet은 테 넌 트 액세스를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="70b21-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70b21-107">EXAMPLES</span></span>

### <span data-ttu-id="70b21-108">예제 1: 테 넌 트 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="70b21-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="70b21-109">이 명령은 지정 된 컨텍스트에서 테 넌 트 액세스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="70b21-110">변수</span><span class="sxs-lookup"><span data-stu-id="70b21-110">PARAMETERS</span></span>

### <span data-ttu-id="70b21-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="70b21-111">-Context</span></span>
<span data-ttu-id="70b21-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="70b21-113">-사용</span><span class="sxs-lookup"><span data-stu-id="70b21-113">-Enabled</span></span>
<span data-ttu-id="70b21-114">이 cmdlet이 테 넌 트 액세스를 사용할지 또는 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="70b21-115">사용 하거나 사용 하지 않을 $False $True 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-115">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b21-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70b21-116">-PassThru</span></span>
<span data-ttu-id="70b21-117">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementAccessInformation** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70b21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b21-118">-DefaultProfile</span></span>
<span data-ttu-id="70b21-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70b21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b21-120">CommonParameters</span></span>
<span data-ttu-id="70b21-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b21-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b21-123">입력</span><span class="sxs-lookup"><span data-stu-id="70b21-123">INPUTS</span></span>

## <span data-ttu-id="70b21-124">출력</span><span class="sxs-lookup"><span data-stu-id="70b21-124">OUTPUTS</span></span>

### <span data-ttu-id="70b21-125">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="70b21-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="70b21-126">상속자</span><span class="sxs-lookup"><span data-stu-id="70b21-126">NOTES</span></span>

## <span data-ttu-id="70b21-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70b21-127">RELATED LINKS</span></span>

[<span data-ttu-id="70b21-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="70b21-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


