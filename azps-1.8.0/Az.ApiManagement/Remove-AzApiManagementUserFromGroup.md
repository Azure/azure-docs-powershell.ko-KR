---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 20c6894f91e92c6f70f5f753d26fe4d76a391e70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869386"
---
# <span data-ttu-id="0778d-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="0778d-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="0778d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0778d-102">SYNOPSIS</span></span>
<span data-ttu-id="0778d-103">그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-103">Removes a user from a group.</span></span>

## <span data-ttu-id="0778d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0778d-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0778d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0778d-105">DESCRIPTION</span></span>
<span data-ttu-id="0778d-106">**Remove-AzApiManagementUserFromGroup** cmdlet은 기존 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="0778d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0778d-107">EXAMPLES</span></span>

### <span data-ttu-id="0778d-108">예제 1: 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0778d-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="0778d-109">이 명령은 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="0778d-110">변수</span><span class="sxs-lookup"><span data-stu-id="0778d-110">PARAMETERS</span></span>

### <span data-ttu-id="0778d-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0778d-111">-Context</span></span>
<span data-ttu-id="0778d-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0778d-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0778d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0778d-114">-DefaultProfile</span></span>
<span data-ttu-id="0778d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0778d-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0778d-116">-GroupId</span></span>
<span data-ttu-id="0778d-117">사용자를 제거할 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="0778d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0778d-118">-PassThru</span></span>
<span data-ttu-id="0778d-119">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0778d-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="0778d-120">-UserId</span></span>
<span data-ttu-id="0778d-121">그룹에서 제거할 사용자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="0778d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0778d-122">CommonParameters</span></span>
<span data-ttu-id="0778d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0778d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0778d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0778d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0778d-125">입력</span><span class="sxs-lookup"><span data-stu-id="0778d-125">INPUTS</span></span>

### <span data-ttu-id="0778d-126">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0778d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0778d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0778d-127">System.String</span></span>

### <span data-ttu-id="0778d-128">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0778d-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0778d-129">출력</span><span class="sxs-lookup"><span data-stu-id="0778d-129">OUTPUTS</span></span>

### <span data-ttu-id="0778d-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0778d-130">System.Boolean</span></span>

## <span data-ttu-id="0778d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0778d-131">NOTES</span></span>

## <span data-ttu-id="0778d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0778d-132">RELATED LINKS</span></span>

[<span data-ttu-id="0778d-133">추가-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="0778d-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="0778d-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0778d-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


