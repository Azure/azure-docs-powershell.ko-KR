---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: dbc1baa96b62e907fd1707bd4ccb4fe007d51ec6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697920"
---
# <span data-ttu-id="49ba8-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="49ba8-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="49ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="49ba8-103">테 넌 트 액세스를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="49ba8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49ba8-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49ba8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="49ba8-106">**AzApiManagementTenantAccess** cmdlet은 테 넌 트 액세스를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="49ba8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="49ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="49ba8-108">예제 1: 테 넌 트 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="49ba8-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="49ba8-109">이 명령은 지정 된 컨텍스트에서 테 넌 트 액세스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="49ba8-110">변수</span><span class="sxs-lookup"><span data-stu-id="49ba8-110">PARAMETERS</span></span>

### <span data-ttu-id="49ba8-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="49ba8-111">-Context</span></span>
<span data-ttu-id="49ba8-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="49ba8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ba8-113">-DefaultProfile</span></span>
<span data-ttu-id="49ba8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49ba8-115">-사용</span><span class="sxs-lookup"><span data-stu-id="49ba8-115">-Enabled</span></span>
<span data-ttu-id="49ba8-116">이 cmdlet이 테 넌 트 액세스를 사용할지 또는 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="49ba8-117">사용 하거나 사용 하지 않을 $False $True 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="49ba8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49ba8-118">-PassThru</span></span>
<span data-ttu-id="49ba8-119">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementAccessInformation** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="49ba8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ba8-120">CommonParameters</span></span>
<span data-ttu-id="49ba8-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ba8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ba8-122">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49ba8-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ba8-123">입력</span><span class="sxs-lookup"><span data-stu-id="49ba8-123">INPUTS</span></span>

### <span data-ttu-id="49ba8-124">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="49ba8-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49ba8-125">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="49ba8-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="49ba8-126">출력</span><span class="sxs-lookup"><span data-stu-id="49ba8-126">OUTPUTS</span></span>

### <span data-ttu-id="49ba8-127">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="49ba8-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="49ba8-128">상속자</span><span class="sxs-lookup"><span data-stu-id="49ba8-128">NOTES</span></span>

## <span data-ttu-id="49ba8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49ba8-129">RELATED LINKS</span></span>

[<span data-ttu-id="49ba8-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="49ba8-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


