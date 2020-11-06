---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536495"
---
# <span data-ttu-id="8f7be-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="8f7be-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="8f7be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7be-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7be-103">서버 장기 보존 자격 증명 모음을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f7be-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f7be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f7be-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7be-106">**AzureRmSqlServerBackupLongTermRetentionVault** cmdlet은이 서버에 등록 된 장기 보존 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="8f7be-107">자격 증명 모음은 백업 데이터를 저장 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="8f7be-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8f7be-108">EXAMPLES</span></span>

## <span data-ttu-id="8f7be-109">변수</span><span class="sxs-lookup"><span data-stu-id="8f7be-109">PARAMETERS</span></span>

### <span data-ttu-id="8f7be-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7be-110">-DefaultProfile</span></span>
<span data-ttu-id="8f7be-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f7be-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f7be-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7be-112">-ResourceGroupName</span></span>
<span data-ttu-id="8f7be-113">서버를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="8f7be-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7be-114">-ResourceId</span></span>
<span data-ttu-id="8f7be-115">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7be-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f7be-116">-ServerName</span></span>
<span data-ttu-id="8f7be-117">이 cmdlet이 자격 증명 모음을 설정 하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-117">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="8f7be-118">-확인</span><span class="sxs-lookup"><span data-stu-id="8f7be-118">-Confirm</span></span>
<span data-ttu-id="8f7be-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7be-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7be-120">-WhatIf</span></span>
<span data-ttu-id="8f7be-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7be-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7be-123">CommonParameters</span></span>
<span data-ttu-id="8f7be-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7be-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7be-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7be-126">입력</span><span class="sxs-lookup"><span data-stu-id="8f7be-126">INPUTS</span></span>

### <span data-ttu-id="8f7be-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f7be-127">System.String</span></span>

## <span data-ttu-id="8f7be-128">출력</span><span class="sxs-lookup"><span data-stu-id="8f7be-128">OUTPUTS</span></span>

### <span data-ttu-id="8f7be-129">AzureSqlServerBackupLongTermRetentionVaultModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="8f7be-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="8f7be-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8f7be-130">NOTES</span></span>

## <span data-ttu-id="8f7be-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f7be-131">RELATED LINKS</span></span>

[<span data-ttu-id="8f7be-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="8f7be-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="8f7be-133">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8f7be-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
