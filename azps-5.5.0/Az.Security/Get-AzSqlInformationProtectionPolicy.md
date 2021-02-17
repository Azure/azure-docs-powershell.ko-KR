---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198724"
---
# <span data-ttu-id="efb29-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="efb29-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="efb29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb29-102">SYNOPSIS</span></span>
<span data-ttu-id="efb29-103">정보 보호 정책에 대한 SQL 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="efb29-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="efb29-104">구문</span><span class="sxs-lookup"><span data-stu-id="efb29-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efb29-105">설명</span><span class="sxs-lookup"><span data-stu-id="efb29-105">DESCRIPTION</span></span>
<span data-ttu-id="efb29-106">정보 보호 정책에 대한 SQL 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="efb29-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="efb29-107">예제</span><span class="sxs-lookup"><span data-stu-id="efb29-107">EXAMPLES</span></span>

### <span data-ttu-id="efb29-108">예제</span><span class="sxs-lookup"><span data-stu-id="efb29-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="efb29-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efb29-109">PARAMETERS</span></span>

### <span data-ttu-id="efb29-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efb29-110">-AsJob</span></span>
<span data-ttu-id="efb29-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="efb29-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efb29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb29-112">-DefaultProfile</span></span>
<span data-ttu-id="efb29-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efb29-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb29-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb29-114">CommonParameters</span></span>
<span data-ttu-id="efb29-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efb29-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb29-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="efb29-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb29-117">입력</span><span class="sxs-lookup"><span data-stu-id="efb29-117">INPUTS</span></span>

### <span data-ttu-id="efb29-118">System.string</span><span class="sxs-lookup"><span data-stu-id="efb29-118">System.string</span></span>

## <span data-ttu-id="efb29-119">출력</span><span class="sxs-lookup"><span data-stu-id="efb29-119">OUTPUTS</span></span>

### <span data-ttu-id="efb29-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="efb29-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="efb29-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efb29-121">NOTES</span></span>

## <span data-ttu-id="efb29-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efb29-122">RELATED LINKS</span></span>
