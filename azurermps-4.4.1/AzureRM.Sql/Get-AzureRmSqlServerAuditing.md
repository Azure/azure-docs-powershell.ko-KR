---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529996"
---
# <span data-ttu-id="120d3-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="120d3-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="120d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120d3-102">SYNOPSIS</span></span>
<span data-ttu-id="120d3-103">Azure SQL server의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="120d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="120d3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="120d3-105">DESCRIPTION</span></span>
<span data-ttu-id="120d3-106">**AzureRmSqlServerAuditing** Cmdlet은 Azure SQL server의 blob 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="120d3-107">데이터베이스를 식별 하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="120d3-108">이 cmdlet는 지정 된 Azure SQL server에 정의 된 Azure SQL 데이터베이스에서 사용 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="120d3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="120d3-109">EXAMPLES</span></span>

### <span data-ttu-id="120d3-110">예제 1: Azure SQL server의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="120d3-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="120d3-111">변수</span><span class="sxs-lookup"><span data-stu-id="120d3-111">PARAMETERS</span></span>

### <span data-ttu-id="120d3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120d3-112">-ResourceGroupName</span></span>
<span data-ttu-id="120d3-113">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="120d3-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="120d3-114">-ServerName</span></span>
<span data-ttu-id="120d3-115">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-115">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="120d3-116">-확인</span><span class="sxs-lookup"><span data-stu-id="120d3-116">-Confirm</span></span>
<span data-ttu-id="120d3-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120d3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120d3-118">-WhatIf</span></span>
<span data-ttu-id="120d3-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="120d3-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120d3-121">-DefaultProfile</span></span>
<span data-ttu-id="120d3-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="120d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120d3-123">CommonParameters</span></span>
<span data-ttu-id="120d3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="120d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120d3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120d3-126">입력</span><span class="sxs-lookup"><span data-stu-id="120d3-126">INPUTS</span></span>

## <span data-ttu-id="120d3-127">출력</span><span class="sxs-lookup"><span data-stu-id="120d3-127">OUTPUTS</span></span>

### <span data-ttu-id="120d3-128">Microsoft. Test.sql. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="120d3-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="120d3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="120d3-129">NOTES</span></span>

## <span data-ttu-id="120d3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="120d3-130">RELATED LINKS</span></span>

