---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877701"
---
# <span data-ttu-id="a58be-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a58be-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="a58be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58be-102">SYNOPSIS</span></span>
<span data-ttu-id="a58be-103">현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a58be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a58be-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a58be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a58be-105">DESCRIPTION</span></span>
<span data-ttu-id="a58be-106">현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a58be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a58be-107">EXAMPLES</span></span>

### <span data-ttu-id="a58be-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a58be-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="a58be-109">관리 파트너 제거</span><span class="sxs-lookup"><span data-stu-id="a58be-109">Remove management partner</span></span>

## <span data-ttu-id="a58be-110">변수</span><span class="sxs-lookup"><span data-stu-id="a58be-110">PARAMETERS</span></span>

### <span data-ttu-id="a58be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58be-111">-DefaultProfile</span></span>
<span data-ttu-id="a58be-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58be-113">-(또는)-(Id)</span><span class="sxs-lookup"><span data-stu-id="a58be-113">-PartnerId</span></span>
<span data-ttu-id="a58be-114">관리 파트너 id로 6 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58be-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a58be-115">-PassThru</span></span>
<span data-ttu-id="a58be-116">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a58be-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a58be-117">-확인</span><span class="sxs-lookup"><span data-stu-id="a58be-117">-Confirm</span></span>
<span data-ttu-id="a58be-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58be-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58be-119">-WhatIf</span></span>
<span data-ttu-id="a58be-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58be-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58be-122">CommonParameters</span></span>
<span data-ttu-id="a58be-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58be-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a58be-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58be-125">입력</span><span class="sxs-lookup"><span data-stu-id="a58be-125">INPUTS</span></span>

### <span data-ttu-id="a58be-126">않아야</span><span class="sxs-lookup"><span data-stu-id="a58be-126">None</span></span>

## <span data-ttu-id="a58be-127">출력</span><span class="sxs-lookup"><span data-stu-id="a58be-127">OUTPUTS</span></span>

### <span data-ttu-id="a58be-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a58be-128">System.Boolean</span></span>

## <span data-ttu-id="a58be-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a58be-129">NOTES</span></span>

## <span data-ttu-id="a58be-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a58be-130">RELATED LINKS</span></span>

[<span data-ttu-id="a58be-131">새로운 AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a58be-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="a58be-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a58be-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="a58be-133">업데이트-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a58be-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)