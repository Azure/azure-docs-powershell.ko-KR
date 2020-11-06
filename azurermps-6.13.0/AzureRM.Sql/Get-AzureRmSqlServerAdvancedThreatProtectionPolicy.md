---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531919"
---
# <span data-ttu-id="ba30c-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30c-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="ba30c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba30c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba30c-103">서버의 고급 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba30c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba30c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba30c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba30c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba30c-106">**AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet은 서버의 고급 위협 보호 정책을 retrives 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="ba30c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba30c-107">EXAMPLES</span></span>

### <span data-ttu-id="ba30c-108">예제 1-서버 고급 위협 방지 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="ba30c-109">예제 2-서버 리소스에서 서버 고급 위협 방지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="ba30c-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba30c-110">PARAMETERS</span></span>

### <span data-ttu-id="ba30c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba30c-111">-DefaultProfile</span></span>
<span data-ttu-id="ba30c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba30c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba30c-113">-InputObject</span></span>
<span data-ttu-id="ba30c-114">고급 위협 보호 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="ba30c-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba30c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba30c-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba30c-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba30c-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba30c-117">-ServerName</span></span>
<span data-ttu-id="ba30c-118">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="ba30c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba30c-119">CommonParameters</span></span>
<span data-ttu-id="ba30c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba30c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba30c-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba30c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba30c-122">입력</span><span class="sxs-lookup"><span data-stu-id="ba30c-122">INPUTS</span></span>

### <span data-ttu-id="ba30c-123">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="ba30c-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="ba30c-124">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba30c-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ba30c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba30c-125">System.String</span></span>

## <span data-ttu-id="ba30c-126">출력</span><span class="sxs-lookup"><span data-stu-id="ba30c-126">OUTPUTS</span></span>

### <span data-ttu-id="ba30c-127">AdvancedThreatProtection. ServerAdvancedThreatProtectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="ba30c-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="ba30c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ba30c-128">NOTES</span></span>

## <span data-ttu-id="ba30c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba30c-129">RELATED LINKS</span></span>
