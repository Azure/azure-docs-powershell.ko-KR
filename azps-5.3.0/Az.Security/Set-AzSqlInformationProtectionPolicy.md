---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494961"
---
# <span data-ttu-id="da4cb-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da4cb-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="da4cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="da4cb-103">정보 보호 정책을 SQL 테넌트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="da4cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="da4cb-104">SYNTAX</span></span>

### <span data-ttu-id="da4cb-105">SQL 보호 정책(기본값)</span><span class="sxs-lookup"><span data-stu-id="da4cb-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da4cb-106">SQL 보호 정책 파일 경로</span><span class="sxs-lookup"><span data-stu-id="da4cb-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da4cb-107">설명</span><span class="sxs-lookup"><span data-stu-id="da4cb-107">DESCRIPTION</span></span>
<span data-ttu-id="da4cb-108">정보 보호 정책을 SQL 테넌트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="da4cb-109">예제</span><span class="sxs-lookup"><span data-stu-id="da4cb-109">EXAMPLES</span></span>

### <span data-ttu-id="da4cb-110">예제</span><span class="sxs-lookup"><span data-stu-id="da4cb-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="da4cb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da4cb-111">PARAMETERS</span></span>

### <span data-ttu-id="da4cb-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da4cb-112">-AsJob</span></span>
<span data-ttu-id="da4cb-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="da4cb-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da4cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4cb-114">-DefaultProfile</span></span>
<span data-ttu-id="da4cb-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da4cb-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="da4cb-116">-FilePath</span></span>
<span data-ttu-id="da4cb-117">정보 보호 정책 정의를 포함하는 .json SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="da4cb-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="da4cb-118">-Policy</span></span>
<span data-ttu-id="da4cb-119">정보 보호 SQL 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="da4cb-120">정책을 정의하는 .json 파일 또는 JSON 형식 문자열의 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="da4cb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da4cb-121">-Confirm</span></span>
<span data-ttu-id="da4cb-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da4cb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da4cb-123">-WhatIf</span></span>
<span data-ttu-id="da4cb-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da4cb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da4cb-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da4cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4cb-126">CommonParameters</span></span>
<span data-ttu-id="da4cb-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da4cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4cb-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da4cb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4cb-129">입력</span><span class="sxs-lookup"><span data-stu-id="da4cb-129">INPUTS</span></span>

### <span data-ttu-id="da4cb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="da4cb-130">System.String</span></span>

## <span data-ttu-id="da4cb-131">출력</span><span class="sxs-lookup"><span data-stu-id="da4cb-131">OUTPUTS</span></span>

### <span data-ttu-id="da4cb-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da4cb-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="da4cb-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da4cb-133">NOTES</span></span>

## <span data-ttu-id="da4cb-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da4cb-134">RELATED LINKS</span></span>
