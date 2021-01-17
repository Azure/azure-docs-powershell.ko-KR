---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360025"
---
# <span data-ttu-id="553c2-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="553c2-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="553c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="553c2-102">SYNOPSIS</span></span>
<span data-ttu-id="553c2-103">ANF(Azure NetApp Files) 계정 백업 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="553c2-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="553c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="553c2-104">SYNTAX</span></span>

### <span data-ttu-id="553c2-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="553c2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="553c2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="553c2-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="553c2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="553c2-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="553c2-108">설명</span><span class="sxs-lookup"><span data-stu-id="553c2-108">DESCRIPTION</span></span>
<span data-ttu-id="553c2-109">**Get-AzNetAppFilesVault** cmdlet은 ANF 계정 백업 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="553c2-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="553c2-110">예제</span><span class="sxs-lookup"><span data-stu-id="553c2-110">EXAMPLES</span></span>

### <span data-ttu-id="553c2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="553c2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="553c2-112">이 명령은 ANF(Azure NetappFiles) 계정 "MyAnfAccount"에 대한 백업 자격 증명 모음 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="553c2-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="553c2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="553c2-113">PARAMETERS</span></span>

### <span data-ttu-id="553c2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="553c2-114">-AccountName</span></span>
<span data-ttu-id="553c2-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="553c2-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553c2-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="553c2-116">-AccountObject</span></span>
<span data-ttu-id="553c2-117">새 백업 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="553c2-117">The account for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553c2-118">-DefaultProfile</span></span>
<span data-ttu-id="553c2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="553c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="553c2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553c2-120">-ResourceGroupName</span></span>
<span data-ttu-id="553c2-121">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="553c2-121">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553c2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="553c2-122">-ResourceId</span></span>
<span data-ttu-id="553c2-123">ANF 풀의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="553c2-123">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553c2-124">CommonParameters</span></span>
<span data-ttu-id="553c2-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="553c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553c2-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="553c2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553c2-127">입력</span><span class="sxs-lookup"><span data-stu-id="553c2-127">INPUTS</span></span>

### <span data-ttu-id="553c2-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="553c2-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="553c2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="553c2-129">System.String</span></span>

## <span data-ttu-id="553c2-130">출력</span><span class="sxs-lookup"><span data-stu-id="553c2-130">OUTPUTS</span></span>

### <span data-ttu-id="553c2-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="553c2-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="553c2-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="553c2-132">NOTES</span></span>

## <span data-ttu-id="553c2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="553c2-133">RELATED LINKS</span></span>
