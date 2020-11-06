---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 0cabae7f7b803001a03b64eec027925733d05545
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533820"
---
# <span data-ttu-id="2f82c-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="2f82c-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="2f82c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f82c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f82c-103">데이터베이스 서버 시스템 복구 구성에 대 한 활동을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f82c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f82c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f82c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f82c-105">DESCRIPTION</span></span>
<span data-ttu-id="2f82c-106">**AzureRmSqlServerDisasterRecoveryConfigurationActivity** CMDLET은 SQL 데이터베이스 서버 시스템 복구 구성에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2f82c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2f82c-107">EXAMPLES</span></span>

## <span data-ttu-id="2f82c-108">변수</span><span class="sxs-lookup"><span data-stu-id="2f82c-108">PARAMETERS</span></span>

### <span data-ttu-id="2f82c-109">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2f82c-109">-OperationId</span></span>
<span data-ttu-id="2f82c-110">작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-110">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f82c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f82c-111">-ResourceGroupName</span></span>
<span data-ttu-id="2f82c-112">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2f82c-113">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2f82c-113">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="2f82c-114">서버 시스템 복구 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-114">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="2f82c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f82c-115">-ServerName</span></span>
<span data-ttu-id="2f82c-116">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2f82c-117">-확인</span><span class="sxs-lookup"><span data-stu-id="2f82c-117">-Confirm</span></span>
<span data-ttu-id="2f82c-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f82c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f82c-119">-WhatIf</span></span>
<span data-ttu-id="2f82c-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f82c-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f82c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f82c-122">-DefaultProfile</span></span>
<span data-ttu-id="2f82c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f82c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f82c-124">CommonParameters</span></span>
<span data-ttu-id="2f82c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f82c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f82c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f82c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f82c-127">입력</span><span class="sxs-lookup"><span data-stu-id="2f82c-127">INPUTS</span></span>

## <span data-ttu-id="2f82c-128">출력</span><span class="sxs-lookup"><span data-stu-id="2f82c-128">OUTPUTS</span></span>

## <span data-ttu-id="2f82c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="2f82c-129">NOTES</span></span>

## <span data-ttu-id="2f82c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f82c-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f82c-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2f82c-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
