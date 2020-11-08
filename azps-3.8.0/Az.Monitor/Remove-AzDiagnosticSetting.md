---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878966"
---
# <span data-ttu-id="b64e3-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b64e3-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="b64e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b64e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b64e3-103">A 리소스에 대 한 진단 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="b64e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b64e3-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b64e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b64e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b64e3-106">**AzDiagnosticSetting** cmdlet은 특정 리소스에 대 한 진단 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="b64e3-107">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b64e3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b64e3-108">EXAMPLES</span></span>

### <span data-ttu-id="b64e3-109">예제 1: 리소스에 대 한 기본 진단 설정 (서비스) 제거</span><span class="sxs-lookup"><span data-stu-id="b64e3-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="b64e3-110">이 명령은 Resource01 이라는 리소스에 대 한 기본 진단 설정 (서비스)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="b64e3-111">예제 2: 리소스에 대해 지정 된 이름으로 식별 되는 기본 진단 설정 제거</span><span class="sxs-lookup"><span data-stu-id="b64e3-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="b64e3-112">이 명령은 Resource01 이라는 리소스에 대해 myDiagSetting 이라는 진단 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="b64e3-113">변수</span><span class="sxs-lookup"><span data-stu-id="b64e3-113">PARAMETERS</span></span>

### <span data-ttu-id="b64e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64e3-114">-DefaultProfile</span></span>
<span data-ttu-id="b64e3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64e3-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b64e3-116">-Name</span></span>
<span data-ttu-id="b64e3-117">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="b64e3-118">이전 API 에서처럼 "service"로 통화를 지정 하지 않으면이 cmdlet은 메트릭/로그의 모든 범주를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b64e3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b64e3-119">-ResourceId</span></span>
<span data-ttu-id="b64e3-120">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="b64e3-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b64e3-121">-Confirm</span></span>
<span data-ttu-id="b64e3-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64e3-123">-WhatIf</span></span>
<span data-ttu-id="b64e3-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b64e3-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64e3-126">CommonParameters</span></span>
<span data-ttu-id="b64e3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b64e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64e3-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b64e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64e3-129">입력</span><span class="sxs-lookup"><span data-stu-id="b64e3-129">INPUTS</span></span>

### <span data-ttu-id="b64e3-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b64e3-130">System.String</span></span>

## <span data-ttu-id="b64e3-131">출력</span><span class="sxs-lookup"><span data-stu-id="b64e3-131">OUTPUTS</span></span>

### <span data-ttu-id="b64e3-132">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b64e3-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b64e3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b64e3-133">NOTES</span></span>

## <span data-ttu-id="b64e3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b64e3-134">RELATED LINKS</span></span>

<span data-ttu-id="b64e3-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="b64e3-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>