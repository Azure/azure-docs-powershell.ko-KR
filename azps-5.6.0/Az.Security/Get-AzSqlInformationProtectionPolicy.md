---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: da881ceac74810b05385b26f54b7c498c60c2e77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987532"
---
# <span data-ttu-id="0bf0e-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf0e-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="0bf0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf0e-103">효과적인 테넌트 SQL 보호 정책을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf0e-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="0bf0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0bf0e-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf0e-105">설명</span><span class="sxs-lookup"><span data-stu-id="0bf0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf0e-106">효과적인 테넌트 SQL 보호 정책을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf0e-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="0bf0e-107">예제</span><span class="sxs-lookup"><span data-stu-id="0bf0e-107">EXAMPLES</span></span>

### <span data-ttu-id="0bf0e-108">예제</span><span class="sxs-lookup"><span data-stu-id="0bf0e-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="0bf0e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0bf0e-109">PARAMETERS</span></span>

### <span data-ttu-id="0bf0e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bf0e-110">-AsJob</span></span>
<span data-ttu-id="0bf0e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0bf0e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bf0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf0e-112">-DefaultProfile</span></span>
<span data-ttu-id="0bf0e-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf0e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bf0e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf0e-114">CommonParameters</span></span>
<span data-ttu-id="0bf0e-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf0e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf0e-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bf0e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf0e-117">입력</span><span class="sxs-lookup"><span data-stu-id="0bf0e-117">INPUTS</span></span>

### <span data-ttu-id="0bf0e-118">System.string</span><span class="sxs-lookup"><span data-stu-id="0bf0e-118">System.string</span></span>

## <span data-ttu-id="0bf0e-119">출력</span><span class="sxs-lookup"><span data-stu-id="0bf0e-119">OUTPUTS</span></span>

### <span data-ttu-id="0bf0e-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf0e-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="0bf0e-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0bf0e-121">NOTES</span></span>

## <span data-ttu-id="0bf0e-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bf0e-122">RELATED LINKS</span></span>
