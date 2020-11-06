---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528785"
---
# <span data-ttu-id="57881-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="57881-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="57881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57881-102">SYNOPSIS</span></span>
<span data-ttu-id="57881-103">Azure SQL server의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57881-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57881-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57881-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57881-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57881-105">DESCRIPTION</span></span>
<span data-ttu-id="57881-106">**AzureRmSqlServerAuditing** Cmdlet은 Azure SQL server의 blob 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57881-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="57881-107">데이터베이스를 식별 하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57881-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="57881-108">이 cmdlet는 지정 된 Azure SQL server에 정의 된 Azure SQL 데이터베이스에서 사용 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="57881-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="57881-109">예제의</span><span class="sxs-lookup"><span data-stu-id="57881-109">EXAMPLES</span></span>

### <span data-ttu-id="57881-110">예제 1: Azure SQL server의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="57881-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="57881-111">변수</span><span class="sxs-lookup"><span data-stu-id="57881-111">PARAMETERS</span></span>

### <span data-ttu-id="57881-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57881-112">-DefaultProfile</span></span>
<span data-ttu-id="57881-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="57881-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57881-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57881-114">-ResourceGroupName</span></span>
<span data-ttu-id="57881-115">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57881-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="57881-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57881-116">-ServerName</span></span>
<span data-ttu-id="57881-117">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57881-117">SQL server name.</span></span>

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

### <span data-ttu-id="57881-118">-확인</span><span class="sxs-lookup"><span data-stu-id="57881-118">-Confirm</span></span>
<span data-ttu-id="57881-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57881-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57881-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57881-120">-WhatIf</span></span>
<span data-ttu-id="57881-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57881-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57881-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57881-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57881-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57881-123">CommonParameters</span></span>
<span data-ttu-id="57881-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57881-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57881-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57881-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57881-126">입력</span><span class="sxs-lookup"><span data-stu-id="57881-126">INPUTS</span></span>

### <span data-ttu-id="57881-127">않아야</span><span class="sxs-lookup"><span data-stu-id="57881-127">None</span></span>
<span data-ttu-id="57881-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57881-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57881-129">출력</span><span class="sxs-lookup"><span data-stu-id="57881-129">OUTPUTS</span></span>

### <span data-ttu-id="57881-130">Microsoft. Test.sql. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="57881-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="57881-131">상속자</span><span class="sxs-lookup"><span data-stu-id="57881-131">NOTES</span></span>

## <span data-ttu-id="57881-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57881-132">RELATED LINKS</span></span>
