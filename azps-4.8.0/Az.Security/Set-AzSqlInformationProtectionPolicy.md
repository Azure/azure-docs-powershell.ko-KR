---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204332"
---
# <span data-ttu-id="d165e-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d165e-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="d165e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d165e-102">SYNOPSIS</span></span>
<span data-ttu-id="d165e-103">효과적인 테 넌 트 SQL 정보 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="d165e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d165e-104">SYNTAX</span></span>

### <span data-ttu-id="d165e-105">SQL 정보 보호 정책 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d165e-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d165e-106">SQL 정보 보호 정책 파일 경로</span><span class="sxs-lookup"><span data-stu-id="d165e-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d165e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d165e-107">DESCRIPTION</span></span>
<span data-ttu-id="d165e-108">효과적인 테 넌 트 SQL 정보 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="d165e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d165e-109">EXAMPLES</span></span>

### <span data-ttu-id="d165e-110">예</span><span class="sxs-lookup"><span data-stu-id="d165e-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="d165e-111">변수</span><span class="sxs-lookup"><span data-stu-id="d165e-111">PARAMETERS</span></span>

### <span data-ttu-id="d165e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d165e-112">-AsJob</span></span>
<span data-ttu-id="d165e-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d165e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d165e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d165e-114">-DefaultProfile</span></span>
<span data-ttu-id="d165e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d165e-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d165e-116">-FilePath</span></span>
<span data-ttu-id="d165e-117">SQL 정보 보호 정책 정의를 포함 하는 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d165e-118">-정책</span><span class="sxs-lookup"><span data-stu-id="d165e-118">-Policy</span></span>
<span data-ttu-id="d165e-119">SQL 정보 보호 정책 정의를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="d165e-120">Json 파일 또는 정책을 정의 하는 JSON 형식 문자열의 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d165e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d165e-121">-Confirm</span></span>
<span data-ttu-id="d165e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d165e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d165e-123">-WhatIf</span></span>
<span data-ttu-id="d165e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d165e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d165e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d165e-126">CommonParameters</span></span>
<span data-ttu-id="d165e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d165e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d165e-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d165e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d165e-129">입력</span><span class="sxs-lookup"><span data-stu-id="d165e-129">INPUTS</span></span>

### <span data-ttu-id="d165e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d165e-130">System.String</span></span>

## <span data-ttu-id="d165e-131">출력</span><span class="sxs-lookup"><span data-stu-id="d165e-131">OUTPUTS</span></span>

### <span data-ttu-id="d165e-132">SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d165e-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="d165e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d165e-133">NOTES</span></span>

## <span data-ttu-id="d165e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d165e-134">RELATED LINKS</span></span>
