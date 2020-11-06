---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528782"
---
# <span data-ttu-id="4e3a3-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="4e3a3-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="4e3a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3a3-103">서버 장기 보존 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e3a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e3a3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4e3a3-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3a3-106">**AzureRmSqlServerBackupLongTermRetentionVault** cmdlet은이 서버에 등록 된 장기 보존 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="4e3a3-107">자격 증명 모음은 백업 데이터를 저장 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="4e3a3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4e3a3-108">EXAMPLES</span></span>

## <span data-ttu-id="4e3a3-109">변수</span><span class="sxs-lookup"><span data-stu-id="4e3a3-109">PARAMETERS</span></span>

### <span data-ttu-id="4e3a3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3a3-110">-DefaultProfile</span></span>
<span data-ttu-id="4e3a3-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4e3a3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e3a3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3a3-112">-ResourceGroupName</span></span>
<span data-ttu-id="4e3a3-113">서버를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="4e3a3-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e3a3-114">-ServerName</span></span>
<span data-ttu-id="4e3a3-115">이 cmdlet이 자격 증명 모음을 가져오는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="4e3a3-116">-확인</span><span class="sxs-lookup"><span data-stu-id="4e3a3-116">-Confirm</span></span>
<span data-ttu-id="4e3a3-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3a3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3a3-118">-WhatIf</span></span>
<span data-ttu-id="4e3a3-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e3a3-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3a3-121">CommonParameters</span></span>
<span data-ttu-id="4e3a3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3a3-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e3a3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3a3-124">입력</span><span class="sxs-lookup"><span data-stu-id="4e3a3-124">INPUTS</span></span>

### <span data-ttu-id="4e3a3-125">않아야</span><span class="sxs-lookup"><span data-stu-id="4e3a3-125">None</span></span>
<span data-ttu-id="4e3a3-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e3a3-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e3a3-127">출력</span><span class="sxs-lookup"><span data-stu-id="4e3a3-127">OUTPUTS</span></span>

## <span data-ttu-id="4e3a3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4e3a3-128">NOTES</span></span>

## <span data-ttu-id="4e3a3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e3a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="4e3a3-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="4e3a3-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="4e3a3-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="4e3a3-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

