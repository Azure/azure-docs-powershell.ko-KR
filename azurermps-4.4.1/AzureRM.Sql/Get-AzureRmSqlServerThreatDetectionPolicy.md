---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 1cb77a435ee951e2e7fe4bc7401e7e4385557eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533816"
---
# <span data-ttu-id="c2e50-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e50-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="c2e50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e50-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e50-103">서버에 대 한 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2e50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2e50-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e50-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2e50-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e50-106">**AzureRmSqlServerThreatDetectionPolicy** Cmdlet은 Azure SQL server의 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="c2e50-107">이 cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 하 여이 cmdlet이 정책을 가져오는 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="c2e50-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c2e50-108">EXAMPLES</span></span>

### <span data-ttu-id="c2e50-109">예제 1: 서버에 대 한 위협 검색 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2e50-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="c2e50-110">이 명령은 Server01 이라는 서버에 대 한 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="c2e50-111">서버가 리소스 그룹 ResourceGroup11에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c2e50-112">변수</span><span class="sxs-lookup"><span data-stu-id="c2e50-112">PARAMETERS</span></span>

### <span data-ttu-id="c2e50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e50-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2e50-114">서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-114">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="c2e50-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c2e50-115">-ServerName</span></span>
<span data-ttu-id="c2e50-116">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c2e50-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c2e50-117">-Confirm</span></span>
<span data-ttu-id="c2e50-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e50-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e50-119">-WhatIf</span></span>
<span data-ttu-id="c2e50-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e50-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e50-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e50-122">-DefaultProfile</span></span>
<span data-ttu-id="c2e50-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2e50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e50-124">CommonParameters</span></span>
<span data-ttu-id="c2e50-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e50-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e50-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e50-127">입력</span><span class="sxs-lookup"><span data-stu-id="c2e50-127">INPUTS</span></span>

## <span data-ttu-id="c2e50-128">출력</span><span class="sxs-lookup"><span data-stu-id="c2e50-128">OUTPUTS</span></span>

### <span data-ttu-id="c2e50-129">ThreatDetection. ServerThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c2e50-129">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="c2e50-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c2e50-130">NOTES</span></span>

## <span data-ttu-id="c2e50-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2e50-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2e50-132">제거-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e50-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="c2e50-133">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c2e50-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


