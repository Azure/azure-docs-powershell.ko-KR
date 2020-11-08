---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048544"
---
# <span data-ttu-id="7c99a-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7c99a-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="7c99a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c99a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c99a-103">기존 API 관리 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="7c99a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c99a-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c99a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c99a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c99a-106">**AzApiManagementGroup** cmdlet은 기존 API 관리 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="7c99a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c99a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c99a-108">예제 1: 기존 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="7c99a-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="7c99a-109">이 명령은 Group0001 이라는 기존 관리 그룹을 제거 하 고 사용자에 게 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="7c99a-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c99a-110">PARAMETERS</span></span>

### <span data-ttu-id="7c99a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7c99a-111">-Context</span></span>
<span data-ttu-id="7c99a-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7c99a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c99a-113">-DefaultProfile</span></span>
<span data-ttu-id="7c99a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c99a-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="7c99a-115">-GroupId</span></span>
<span data-ttu-id="7c99a-116">관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="7c99a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c99a-117">-PassThru</span></span>
<span data-ttu-id="7c99a-118">이 cmdlet이 성공할 경우 $True 값을 반환 하거나, $False 값이 없는 경우, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="7c99a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7c99a-119">-Confirm</span></span>
<span data-ttu-id="7c99a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c99a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c99a-121">-WhatIf</span></span>
<span data-ttu-id="7c99a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c99a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c99a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c99a-124">CommonParameters</span></span>
<span data-ttu-id="7c99a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c99a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c99a-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c99a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c99a-127">입력</span><span class="sxs-lookup"><span data-stu-id="7c99a-127">INPUTS</span></span>

### <span data-ttu-id="7c99a-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7c99a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7c99a-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c99a-129">System.String</span></span>

### <span data-ttu-id="7c99a-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c99a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c99a-131">출력</span><span class="sxs-lookup"><span data-stu-id="7c99a-131">OUTPUTS</span></span>

### <span data-ttu-id="7c99a-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7c99a-132">System.Boolean</span></span>

## <span data-ttu-id="7c99a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7c99a-133">NOTES</span></span>

## <span data-ttu-id="7c99a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c99a-134">RELATED LINKS</span></span>

[<span data-ttu-id="7c99a-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7c99a-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="7c99a-136">새로운 AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7c99a-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="7c99a-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7c99a-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


