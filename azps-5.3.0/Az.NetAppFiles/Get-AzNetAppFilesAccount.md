---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490036"
---
# <span data-ttu-id="c548c-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c548c-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c548c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c548c-102">SYNOPSIS</span></span>
<span data-ttu-id="c548c-103">ANF(Azure NetApp Files) 계정의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c548c-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="c548c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c548c-104">SYNTAX</span></span>

### <span data-ttu-id="c548c-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c548c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c548c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c548c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c548c-107">설명</span><span class="sxs-lookup"><span data-stu-id="c548c-107">DESCRIPTION</span></span>
<span data-ttu-id="c548c-108">**Get-AzNetAppFilesAccount** cmdlet은 ANF 계정의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c548c-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="c548c-109">예제</span><span class="sxs-lookup"><span data-stu-id="c548c-109">EXAMPLES</span></span>

### <span data-ttu-id="c548c-110">예제 1: ANF 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="c548c-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="c548c-111">이 명령은 MyAnfAccount라는 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c548c-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="c548c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c548c-112">PARAMETERS</span></span>

### <span data-ttu-id="c548c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c548c-113">-DefaultProfile</span></span>
<span data-ttu-id="c548c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c548c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c548c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c548c-115">-Name</span></span>
<span data-ttu-id="c548c-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="c548c-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c548c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c548c-117">-ResourceGroupName</span></span>
<span data-ttu-id="c548c-118">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="c548c-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c548c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c548c-119">-ResourceId</span></span>
<span data-ttu-id="c548c-120">ANF 계정의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c548c-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="c548c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c548c-121">CommonParameters</span></span>
<span data-ttu-id="c548c-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c548c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c548c-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c548c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c548c-124">입력</span><span class="sxs-lookup"><span data-stu-id="c548c-124">INPUTS</span></span>

### <span data-ttu-id="c548c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c548c-125">System.String</span></span>

## <span data-ttu-id="c548c-126">출력</span><span class="sxs-lookup"><span data-stu-id="c548c-126">OUTPUTS</span></span>

### <span data-ttu-id="c548c-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c548c-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c548c-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c548c-128">NOTES</span></span>

## <span data-ttu-id="c548c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c548c-129">RELATED LINKS</span></span>
