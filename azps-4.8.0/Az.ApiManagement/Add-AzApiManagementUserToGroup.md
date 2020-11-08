---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94055978"
---
# <span data-ttu-id="1a648-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="1a648-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="1a648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a648-102">SYNOPSIS</span></span>
<span data-ttu-id="1a648-103">그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-103">Adds a user to a group.</span></span>

## <span data-ttu-id="1a648-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a648-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a648-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a648-105">DESCRIPTION</span></span>
<span data-ttu-id="1a648-106">**추가-AzApiManagementUserToGroup** cmdlet은 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="1a648-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a648-107">EXAMPLES</span></span>

### <span data-ttu-id="1a648-108">예제 1: 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="1a648-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="1a648-109">이 명령은 기존 그룹에 기존 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="1a648-110">변수</span><span class="sxs-lookup"><span data-stu-id="1a648-110">PARAMETERS</span></span>

### <span data-ttu-id="1a648-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1a648-111">-Context</span></span>
<span data-ttu-id="1a648-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1a648-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1a648-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a648-114">-DefaultProfile</span></span>
<span data-ttu-id="1a648-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a648-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1a648-116">-GroupId</span></span>
<span data-ttu-id="1a648-117">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-117">Specifies the group ID.</span></span>
<span data-ttu-id="1a648-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1a648-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a648-119">-PassThru</span></span>
<span data-ttu-id="1a648-120">passthru</span><span class="sxs-lookup"><span data-stu-id="1a648-120">passthru</span></span>

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

### <span data-ttu-id="1a648-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="1a648-121">-UserId</span></span>
<span data-ttu-id="1a648-122">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-122">Specifies the user ID.</span></span>
<span data-ttu-id="1a648-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-123">This parameter is required.</span></span>

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

### <span data-ttu-id="1a648-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a648-124">CommonParameters</span></span>
<span data-ttu-id="1a648-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a648-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a648-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a648-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a648-127">입력</span><span class="sxs-lookup"><span data-stu-id="1a648-127">INPUTS</span></span>

### <span data-ttu-id="1a648-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1a648-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1a648-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a648-129">System.String</span></span>

### <span data-ttu-id="1a648-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a648-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a648-131">출력</span><span class="sxs-lookup"><span data-stu-id="1a648-131">OUTPUTS</span></span>

### <span data-ttu-id="1a648-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1a648-132">System.Boolean</span></span>

## <span data-ttu-id="1a648-133">상속자</span><span class="sxs-lookup"><span data-stu-id="1a648-133">NOTES</span></span>

## <span data-ttu-id="1a648-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a648-134">RELATED LINKS</span></span>

[<span data-ttu-id="1a648-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1a648-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="1a648-136">제거-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="1a648-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


