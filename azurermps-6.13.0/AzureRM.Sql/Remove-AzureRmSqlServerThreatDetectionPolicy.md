---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5791d60d6415c71f7e4fa5c52226cd8be7ffbb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531900"
---
# <span data-ttu-id="d639a-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d639a-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="d639a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d639a-102">SYNOPSIS</span></span>
<span data-ttu-id="d639a-103">서버에서 위협 검색 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d639a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d639a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d639a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d639a-105">DESCRIPTION</span></span>
<span data-ttu-id="d639a-106">Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet은 Azure SQL server에서 위협 검색 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="d639a-107">이 cmdlet을 사용 하려면 ResourceGroupName 및 ServerName 매개 변수를 지정 하 여이 cmdlet이 정책을 제거 하는 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="d639a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d639a-108">EXAMPLES</span></span>

### <span data-ttu-id="d639a-109">예제 1: 데이터베이스에 대 한 위협 검색 정책 제거</span><span class="sxs-lookup"><span data-stu-id="d639a-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="d639a-110">이 명령은 Server01 이라는 서버에서 위협 검색 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="d639a-111">변수</span><span class="sxs-lookup"><span data-stu-id="d639a-111">PARAMETERS</span></span>

### <span data-ttu-id="d639a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d639a-112">-DefaultProfile</span></span>
<span data-ttu-id="d639a-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d639a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d639a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d639a-114">-PassThru</span></span>
<span data-ttu-id="d639a-115">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d639a-116">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d639a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d639a-117">-ResourceGroupName</span></span>
<span data-ttu-id="d639a-118">서버가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="d639a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d639a-119">-ServerName</span></span>
<span data-ttu-id="d639a-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="d639a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d639a-121">-Confirm</span></span>
<span data-ttu-id="d639a-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d639a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d639a-123">-WhatIf</span></span>
<span data-ttu-id="d639a-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d639a-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d639a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d639a-126">CommonParameters</span></span>
<span data-ttu-id="d639a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d639a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d639a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d639a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d639a-129">입력</span><span class="sxs-lookup"><span data-stu-id="d639a-129">INPUTS</span></span>

### <span data-ttu-id="d639a-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d639a-130">System.String</span></span>

## <span data-ttu-id="d639a-131">출력</span><span class="sxs-lookup"><span data-stu-id="d639a-131">OUTPUTS</span></span>

### <span data-ttu-id="d639a-132">ThreatDetection. ServerThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d639a-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="d639a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d639a-133">NOTES</span></span>

## <span data-ttu-id="d639a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d639a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d639a-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d639a-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

