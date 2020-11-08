---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047632"
---
# <span data-ttu-id="0ee72-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0ee72-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="0ee72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ee72-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee72-103">효과적인 테 넌 트 SQL 정보 보호 정책을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ee72-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="0ee72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ee72-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ee72-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ee72-105">DESCRIPTION</span></span>
<span data-ttu-id="0ee72-106">효과적인 테 넌 트 SQL 정보 보호 정책을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ee72-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="0ee72-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ee72-107">EXAMPLES</span></span>

### <span data-ttu-id="0ee72-108">예</span><span class="sxs-lookup"><span data-stu-id="0ee72-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="0ee72-109">변수</span><span class="sxs-lookup"><span data-stu-id="0ee72-109">PARAMETERS</span></span>

### <span data-ttu-id="0ee72-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ee72-110">-AsJob</span></span>
<span data-ttu-id="0ee72-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0ee72-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ee72-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee72-112">-DefaultProfile</span></span>
<span data-ttu-id="0ee72-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ee72-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ee72-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee72-114">CommonParameters</span></span>
<span data-ttu-id="0ee72-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ee72-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee72-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ee72-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee72-117">입력</span><span class="sxs-lookup"><span data-stu-id="0ee72-117">INPUTS</span></span>

### <span data-ttu-id="0ee72-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ee72-118">System.string</span></span>

## <span data-ttu-id="0ee72-119">출력</span><span class="sxs-lookup"><span data-stu-id="0ee72-119">OUTPUTS</span></span>

### <span data-ttu-id="0ee72-120">SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="0ee72-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="0ee72-121">상속자</span><span class="sxs-lookup"><span data-stu-id="0ee72-121">NOTES</span></span>

## <span data-ttu-id="0ee72-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ee72-122">RELATED LINKS</span></span>
