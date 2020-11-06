---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531625"
---
# <span data-ttu-id="dc33b-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc33b-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="dc33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc33b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc33b-103">데이터베이스에 대 한 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc33b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc33b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc33b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc33b-105">DESCRIPTION</span></span>
<span data-ttu-id="dc33b-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet은 Azure SQL 데이터베이스의 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="dc33b-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여이 cmdlet이 정책을 가져오는 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="dc33b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dc33b-108">EXAMPLES</span></span>

### <span data-ttu-id="dc33b-109">예제 1: 데이터베이스에 대 한 위협 검색 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="dc33b-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="dc33b-110">이 명령은 Database01 이라는 데이터베이스에 대 한 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="dc33b-111">데이터베이스는 리소스 그룹 ResourceGroup11에 할당 되는 Server01 이라는 서버에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="dc33b-112">변수</span><span class="sxs-lookup"><span data-stu-id="dc33b-112">PARAMETERS</span></span>

### <span data-ttu-id="dc33b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc33b-113">-DatabaseName</span></span>
<span data-ttu-id="dc33b-114">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-114">Specifies the name of a database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc33b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc33b-115">-DefaultProfile</span></span>
<span data-ttu-id="dc33b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dc33b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc33b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc33b-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc33b-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc33b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dc33b-119">-ServerName</span></span>
<span data-ttu-id="dc33b-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-120">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc33b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="dc33b-121">-Confirm</span></span>
<span data-ttu-id="dc33b-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc33b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc33b-123">-WhatIf</span></span>
<span data-ttu-id="dc33b-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc33b-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc33b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc33b-126">CommonParameters</span></span>
<span data-ttu-id="dc33b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc33b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc33b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc33b-129">입력</span><span class="sxs-lookup"><span data-stu-id="dc33b-129">INPUTS</span></span>

###  
<span data-ttu-id="dc33b-130">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="dc33b-131">출력</span><span class="sxs-lookup"><span data-stu-id="dc33b-131">OUTPUTS</span></span>

### <span data-ttu-id="dc33b-132">ThreatDetection. DatabaseThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="dc33b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="dc33b-133">이 cmdlet은 **DatabaseThreatDetectionPolicyModel** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc33b-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="dc33b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="dc33b-134">NOTES</span></span>

## <span data-ttu-id="dc33b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc33b-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc33b-136">제거-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc33b-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



