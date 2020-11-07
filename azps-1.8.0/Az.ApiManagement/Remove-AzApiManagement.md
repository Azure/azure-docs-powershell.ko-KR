---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: 73f30ef12270ce738341e71b0428befe6a3a3ba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869465"
---
# <span data-ttu-id="5877e-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5877e-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="5877e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5877e-102">SYNOPSIS</span></span>
<span data-ttu-id="5877e-103">API Management 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-103">Removes an API Management service.</span></span>

## <span data-ttu-id="5877e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5877e-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5877e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5877e-105">DESCRIPTION</span></span>
<span data-ttu-id="5877e-106">**AzApiManagement** Cmdlet은 Azure API Management 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="5877e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5877e-107">EXAMPLES</span></span>

### <span data-ttu-id="5877e-108">예제 1: API Management 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="5877e-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="5877e-109">이 명령은 ContosoApi 이라는 API Management 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="5877e-110">변수</span><span class="sxs-lookup"><span data-stu-id="5877e-110">PARAMETERS</span></span>

### <span data-ttu-id="5877e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5877e-111">-DefaultProfile</span></span>
<span data-ttu-id="5877e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5877e-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5877e-113">-Name</span></span>
<span data-ttu-id="5877e-114">이 cmdlet이 제거 하는 API 관리 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5877e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5877e-115">-PassThru</span></span>
<span data-ttu-id="5877e-116">작업이 성공할 경우이 cmdlet이 $True 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5877e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5877e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5877e-118">API Management 배포가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="5877e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5877e-119">-Confirm</span></span>
<span data-ttu-id="5877e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5877e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5877e-121">-WhatIf</span></span>
<span data-ttu-id="5877e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5877e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5877e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5877e-124">CommonParameters</span></span>
<span data-ttu-id="5877e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5877e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5877e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5877e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5877e-127">입력</span><span class="sxs-lookup"><span data-stu-id="5877e-127">INPUTS</span></span>

### <span data-ttu-id="5877e-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5877e-128">System.String</span></span>

## <span data-ttu-id="5877e-129">출력</span><span class="sxs-lookup"><span data-stu-id="5877e-129">OUTPUTS</span></span>

### <span data-ttu-id="5877e-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5877e-130">System.Boolean</span></span>

## <span data-ttu-id="5877e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5877e-131">NOTES</span></span>

## <span data-ttu-id="5877e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5877e-132">RELATED LINKS</span></span>

[<span data-ttu-id="5877e-133">백업-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5877e-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="5877e-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5877e-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="5877e-135">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5877e-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="5877e-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5877e-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


